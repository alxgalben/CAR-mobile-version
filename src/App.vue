

<template>
<div class="all" style="height: 100vh;">
  <div class="car-preview-card card" style="width: 22.2rem; height: 37.2rem;">
  <div class="card-body">
    <div class="image-preview card" style="width: 20rem; height: 20rem; overflow: hidden; position: relative;">
      <ul style="list-style: none; padding: 16px; display: flex; justify-content: space-between; z-index: 1000;">
        <li>
          <img :src="require('./coming_soon.jpeg')" alt="Coming Soon" class="eticheta">
        </li>
        <li>
          <img :src="require('./eco_car.jpeg')" alt="Eco Car" class="eticheta">
        </li>
        <li>
          <img :src="require('./new_model.jpeg')" alt="New Model" class="eticheta">
        </li>
        <li>
          <img :src="require('./premium_car.jpeg')" alt="Premium Car" class="eticheta">
        </li>
        <li>
          <img :src="require('./promo_car.jpeg')" alt="Promo Car" class="eticheta">
        </li>
      </ul>


    <div class="slider" style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; max-height: fit-content;">
        <img src="https://rentacar.travis.ro/media/volkswagen_passat_2019_1jpg.jpg" alt="Random Car Image" style="width: 100%; height: 100%; object-fit: cover;">
        <img src="https://rentacar.travis.ro/media/toyota_rav4_2022_1jpg.jpg" alt="Random Car Image 2" style="width: 100%; height: 100%; object-fit: cover;">
        <!-- Add more images as needed -->
    </div>
    <div class="indicators">
        <div class="indicator active" onclick="document.querySelector('.slider').style.transform = 'translateX(0%)'; document.querySelectorAll('.indicator').forEach((indicator, i) => { indicator.classList.toggle('active', i === 0); })"></div>
        <div class="indicator" onclick="document.querySelector('.slider').style.transform = 'translateX(-100%)'; document.querySelectorAll('.indicator').forEach((indicator, i) => { indicator.classList.toggle('active', i === 1); })"></div>
        <!-- Add more indicators as needed based on the number of images -->
    </div>
</div>


<div style="display: flex; flex-direction: row; justify-content: space-between; align-items: center;">
    <div>
        <h5 class="card-title" style="margin-bottom: 0 !important;">Volkswagen Touareg</h5>  
        <h5 class="card-title">(4x4 Automat) Diesel</h5>
    </div>
    <div style="text-align: right;">
        <h6 class="card-title" style="font-size: 14px !important; margin-bottom: 0 !important; color: rgba(33, 37, 41, 0.75);">from</h6> 
        <h5 class="card-subtitle" style="font-size: 18px !important; margin-bottom: 0;"><span style="font-weight: bold; font-size: 1.5rem;">5230 € </span></h5>
        <h6 class="card-title" style="font-size: 14px !important; margin-bottom: 0 !important; color: rgba(33, 37, 41, 0.75);">for 365 days</h6> 
    </div>
</div>




      <h6 class="card-subtitle mb-2 text-muted">or similar | Sedan</h6>


    <div class="tags">
      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="calendar" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">2024</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">5</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="analytics" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">Automatic</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="log-out" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">4</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="construct" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">Diesel</span>
      </span>

      <span class="tag location" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="location" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">Timisoara</span>
      </span>
    </div>
    <div style="text-align: center; margin-top: 15px;">
      <button type="button" class="btn btn-dark" style="width: 100%; color: #fff; border-radius: 16px; font-weight: bold;">SEE DETAILS</button>
    </div>
  </div>

  </div>

  <div class="accordion fixed-bottom" id="accordionExample" data-bs-toggle="offcanvas" data-bs-target="#offcanvasBottom">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
        <strong style="font-size: 25px; margin-right: 35px;">45€</strong>
        <span class="btn btn-warning next"><strong>NEXT</strong></span>
      </button>
    </h2>
  </div>
</div>

</div>
</template>

<style>
:root {
  --tag-color-one: rgb(255, 203, 5);
  --tag-color-text-one: rgb(33, 37, 41);
  --tag-color-text-two: rgba(33, 37, 41, 0.75);
}

.all {
  display: flex;
  justify-content: center;
  align-items: center;
}

.car-preview-card {
  border-radius: 24px !important;
}

.image-preview {
  border-radius: 16px !important;
  margin-bottom: 1rem;
}

.tag {
  font-size: 1rem;
  padding: 4px 8px;
  border-radius: 16px;
  margin-right: 5px;
}

.approved {
    background-color: var(--tag-color-one);
    color: var(--tag-color-text-one);
  }

  .location {
    background-color: #fff;
    color: var(--tag-color-text-one);
    border: 1px solid var(--tag-color-one);
  }

.tags {
  width: 100%;
  text-align: left;
  margin-top: 1.2rem;
}

.eticheta {
  width: 48px;
  height: 48px;
}

.slider {
        display: flex;
        transition: transform 0.5s ease-in-out;
    }

    .indicators {
        position: absolute;
        bottom: 1rem;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
    }

    .indicator {
        width: 1rem;
        height: 1rem;
        background-color: #bbb;
        border-radius: 50%;
        margin: 0 5px;
        cursor: pointer;
        border: 2px solid white;
        transition: 0.3s all ease;
    }

    .indicator.active {
      background-color: var(--tag-color-one);
    }
</style>
