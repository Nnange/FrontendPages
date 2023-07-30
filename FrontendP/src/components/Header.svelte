<script lang="ts">
    import type { IUser } from "../Interfaces/IUser";

    const user1: IUser = {
		name: " Awong Nnange",
		position: "Software Developer",
		profilePic: "",
		vacationDays: 0,
		sickDays: 0,
		personalDays: 0
	}
</script>

<div class="Header flex">
    <div class="header1 mx-auto grid grid-cols-3 mt-5">
        <div class="flex border-b">
            <div class="avatar border-2 rounded-full border-rose-500 m-4">
                03
            </div>
            <div class="my-6">
                <p>Welcome back,</p>
                <h1 class="text-3xl font-bold">{user1.name}</h1>
                <p>{user1.position}</p>
            </div>
        </div>
        <div class="col-span-2 flex justify-end border-b">
            <button class="profileButton py-5">view profile</button>
        </div>
        <div class="text-center py-4 border-r">{user1.vacationDays} vacation days left</div>
        <div class="text-center py-4">{user1.sickDays} sick days left</div>
        <div class="text-center py-4 border-l">{user1.personalDays} personal days left</div>
    </div>
</div>


<style>
    .header1{
        border: 2px solid red;
        width: 90%;
        /* height: 10rem; */
        background: white;
        border-radius: 1rem;
    }
    .avatar{
        width: 7rem;
        height: 7rem;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .profileButton{
        border: 2px solid red;
        padding: 1rem;
        margin: 3rem;
        border-radius: 9999px;
    }
</style>