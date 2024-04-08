<script lang="ts">
export let event_title: string ="Test vísó"



</script>

<div class="card">
    <h2 class="event container">{event_title}</h2>
        <div class="card-bottom">
            <div class="event-rating">
                <i class="fa-regular fa-star" onclick="rate"></i>
                <i class="fa-regular fa-star" onclick="rate"></i>
                <i class="fa-regular fa-star" onclick="rate"></i>
                <i class="fa-regular fa-star" onclick="rate"></i>
                <i class="fa-regular fa-star" onclick="rate"></i>
            </div>
            <div class="event-location">
                <a href="">staðsetning</a>
            </div>
        </div>
</div>

<style>

.card{
    display: flex;
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
    width: 100%;
    cursor: pointer;
    background-color: #213547;
    border-radius: 5px;
    flex-direction: column;
}
.card-bottom{
    display: flex;
    flex-direction:row;
}

.event-rating {
  display: flex;
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
    width: 10%;
    cursor: pointer;
    border-radius: 5px;
    margin: 5px;
    align-items: center;
  }
  .event-location {
  display: flex;
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
    width: 10%;
    cursor: pointer;
    border-radius: 5px;
    text-decoration: none;
    align-items: center;
    margin: 5px;
  }
  
.fa-regular{
  display: flex;
  justify-content: flex-end;
  width: 100%;
}
.fa-solid{
  display: flex;
  justify-content: flex-end;
  width: 100%;
}
</style>