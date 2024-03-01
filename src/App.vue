

<template>
<div class="all" style="height: 100vh;">
  <div class="car-preview-card card" style="width: 25rem; height: 37rem;">
  <div class="card-body">
    <div class="image-preview card" style="width: 22.7rem; height: 20rem; overflow: hidden;">
      <img src="https://picsum.photos/800/600" alt="Random Car Image" style="width: 100%; height: 100%; object-fit: cover;">
    </div>


    <div style="display: flex; justify-content: space-between; align-items: center;">
    <h5 class="card-title">Volkswagen Touareg</h5>  
    <div style="display: flex; align-items: center; margin-bottom: .5rem;">
      <ion-icon name="location" style="margin-right: 5px;"></ion-icon>
      <h5 class="card-subtitle" style="font-size: 18px !important; margin: 0;">Timisoara</h5>
    </div>

    </div>

      <h6 class="card-subtitle mb-2 text-muted">or similar | Sedan</h6>


    <div style="display: flex; align-items: center;">
      <h6 class="card-subtitle" style="margin-bottom: 0 !important;">from 14€ / day<span class="total-price"></span></h6>
   </div>
    <div class="tags">
      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person-circle-outline" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">test extrem de lung</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person-circle-outline" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">test</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person-circle-outline" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">testulet lung</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person-circle-outline" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">test nou</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person-circle-outline" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">test</span>
      </span>

      <span class="tag approved" style="display: inline-flex; align-items: center; margin-bottom: 10px;">
        <ion-icon name="person-circle-outline" style="margin-right: 2px; font-size: .9rem !important;"></ion-icon>
        <span style="font-size: 14px;">testulet frumi</span>
      </span>
    </div>
    <div style="text-align: center; margin-top: 15px;">
      <button type="button" class="btn btn-dark" style="width: 100%; color: var(--tag-color-one); border-radius: 16px; font-weight: bold;">SEE DETAILS</button>
    </div>
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

.tags {
  width: 100%;
  text-align: left;
  margin-top: .9rem;
}
</style>

<script>
</script>