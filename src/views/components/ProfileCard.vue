<template>
  <div class="card h-100">
    <div class="p-3 pb-0 card-header">
      <div class="row">
        <div class="col-md-8 d-flex align-items-center">
          <h6 class="mb-0">동아리 Information</h6>
        </div>
        <div class="col-md-4 text-end">
          <a href="javascript:;">
            <i
              class="text-sm fas fa-user-edit text-secondary"
              data-bs-toggle="tooltip"
              data-bs-placement="top"
              title="Edit Profile"
            ></i>
          </a>
        </div>
      </div>
    </div>
    <div class="p-3 card-body">
      <p class="text-sm">
        안녕하세요. 우리 동아리는 뭐시기 뭐시기 우리 동아리는 뭐시기 뭐시기 우리 동아리는 뭐시기 뭐시기 우리 동아리는 뭐시기 뭐시기
      </p>
      <hr class="my-4 horizontal gray-light" />
      <ul class="list-group">
        <li class="pt-0 text-sm border-0 list-group-item ps-0">
          <strong class="text-dark">Name:</strong> &nbsp; 이동수
        </li>
        <li class="text-sm border-0 list-group-item ps-0">
          <strong class="text-dark">Mobile:</strong> &nbsp; 010-2222-2222
        </li>
        <li class="text-sm border-0 list-group-item ps-0">
          <strong class="text-dark">Email:</strong> &nbsp; legend@email.com
        </li>
        <li class="text-sm border-0 list-group-item ps-0">
          <strong class="text-dark">Location:</strong> &nbsp; 수원대학교
        </li>
        <li class="pb-0 border-0 list-group-item ps-0">
          <strong class="text-sm text-dark">Social:</strong> &nbsp;
          <a
            class="py-0 mb-0 btn btn-facebook btn-simple ps-1 pe-2"
            href="javascript:;"
          >
            <i class="fab fa-facebook fa-lg"></i>
          </a>
          <a
            class="py-0 mb-0 btn btn-twitter btn-simple ps-1 pe-2"
            href="javascript:;"
          >
            <i class="fab fa-twitter fa-lg"></i>
          </a>
          <a
            class="py-0 mb-0 btn btn-instagram btn-simple ps-1 pe-2"
            href="javascript:;"
          >
            <i class="fab fa-instagram fa-lg"></i>
          </a>
        </li>


      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileCard",
};
</script>
