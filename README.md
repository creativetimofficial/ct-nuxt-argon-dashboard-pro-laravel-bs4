# [Nuxt Argon Dashboard Pro Laravel BS4](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/?ref=nadpl-readme) [![Tweet](https://img.shields.io/twitter/url/http/shields.io.svg?style=social&logo=twitter)](https://twitter.com/home?status=Nuxt%20Argon%20Dashboard%20Pro%20Laravel%E2%9D%A4%EF%B8%8F%0Ahttps%3A//nuxt-argon-dashboard-pro-larave-bs4l.creative-tim.com/%20%23%nuxt%20%23%argon%20%23design%20%23dashboard%20%23laravel%20%23pro%20via%20%40CreativeTim)

![version](https://img.shields.io/badge/version-1.0.0-blue.svg) [![GitHub issues open](https://img.shields.io/github/issues/creativetimofficial/ct-nuxt-argon-dashboard-pro-laravel-bs4.svg?maxAge=2592000)](https://github.com/creativetimofficial/ct-nuxt-argon-dashboard-pro-laravel-bs4/issues?q=is%3Aopen+is%3Aissue) [![GitHub issues closed](https://img.shields.io/github/issues-closed-raw/creativetimofficial/ct-nuxt-argon-dashboard-pro-laravel-bs4/ct-nuxt-argon-dashboard-pro-laravel-bs4.svg?maxAge=2592000)](https://github.com/creativetimofficial/ct-nuxt-argon-dashboard-pro-laravel-bs4/issues?q=is%3Aissue+is%3Aclosed)

_Frontend version_: Argon Dashboard v1.2.0. More info at https://www.creative-tim.com/product/argon-dashboard-pro

_Nuxt version_: Nuxt Argon Dashboard v1.2.1. More info at https://www.creative-tim.com/product/nuxt-argon-dashboard-pro

![Product Image](https://s3.amazonaws.com/creativetim_bucket/products/732/original/opt_adp_nuxt_laravel_thumbnail.jpg)

What if you could go from frontend to fullstack in an instant when building your app? We partnered with [UPDIVISION](https://updivision.com) to bring you Nuxt Argon Dashboard PRO Laravel, the ultimate fullstack resource. Nuxt Argon Dashboard PRO Laravel comes not only with a huge number of UI components and a Nuxt Argon frontend, but also with an API-powered Laravel backend.

# Download

For the PRO version of the project you will download the .zip file from the Creative Tim site and extract it.

You will get two project folders: one for the Laravel API project and one for the Nuxt frontend.

# Laravel API Setup

## Introduction

JSON:API is a specification for how a client should request that resources be fetched or modified, and how a server should respond to those requests. It is designed to minimize both the number of requests and the amount of data transmitted between clients and servers. This efficiency is achieved without compromising readability, flexibility, or discoverability.

[Click here to go to the JSON:API docs](https://explore.postman.com/api/6357/laravel-jsonapi)

## Prerequisites

### JSON:API backend
The Laravel JSON:API backend project requires a proper multi-threaded web server such as Apache/Nginx environment with PHP, Composer and MySQL.

**Do not use `php artisan serve` as it will result in stalled requests due to the single-threaded nature of the built-in PHP web server.** 

We strongly recommend using [Laradock](https://laradock.io/) for Linux and Mac or [Laragon](https://laragon.org/download/) for Windows if possible.

Other options for your local environment:
- Windows: [How to install WAMP on Windows](https://updivision.com/blog/post/beginner-s-guide-to-setting-up-your-local-development-environment-on-windows)
- Linux: [How to install LAMP on Linux](https://howtoubuntu.org/how-to-install-lamp-on-ubuntu)
- Mac: [How to install MAMP on MAC](https://wpshout.com/quick-guides/how-to-install-mamp-on-your-mac/)

You will also need to install Composer 2: [https://getcomposer.org/doc/00-intro.md](https://getcomposer.org/doc/00-intro.md)

### Nuxt Argon frontend
The Nuxt Argon frontend project requires a working local environment with NodeJS version 8.9 or above (8.11.0+ recommended), npm.

Install Node: https://nodejs.org/ (version 8.11.0+ recommended)

Install NPM: https://www.npmjs.com/get-npm

## Laravel JSON:API Project Installation

1. Navigate in your Laravel API project folder: cd your-laravel-json-api-project
2. Install project dependencies: composer install
3. Create a new .env file: cp .env.example .env
4. Add your own database credentials in the .env file in DB_DATABASE, DB_USERNAME, DB_PASSWORD
5. Create users table: php artisan migrate --seed
6. Generate application key: php artisan key:generate
7. Install Laravel Passport: php artisan passport:install
8. Add your own mailtrap.io credentials in MAIL_USERNAME and MAIL_PASSWORD in the .env file

## Nuxt Argon Dashboard Project Installation
Note: As many packages are deprecated on Node.js v16.x or higher make sure you are using Node.js 14.x(recommended) before strarting this installation.
1. Navigate to your Nuxt Argon Dashboard project folder: `cd your-nuxt-argon-dashbord-project`
2. Install project dependencies: `npm install`
3. Create a new .env file: `cp .env.example .env`
4. `BASE_URL` should contain the URL of your Nuxt Argon Dashboard Project (eg. http://localhost:8080/)
5. `API_BASE_URL` should contain the URL of your Laravel JSON:API Project. (eg. http://localhost:3000/api/v1)
6. Run `npm run dev` to start the application in a local development environment or `npm run build` to build release distributables.

## Usage

To start testing the Pro theme, register as a user or log in using one of the default users:

- admin type - **admin@jsonapi.com** with the password **secret**
- creator type - **creator@jsonapi.com** with the password **secret**
- member type - **member@jsonapi.com** with the password **secret**

In addition to the features included in the free theme, the Pro theme also has a role management example with an updated user management, as well as tag management, category management and item management examples. All the necessary files are installed out of the box and all the needed routes are added to `src\router\index.js`. Keep in mind that all the features can be viewed once you log in using the credentials provided above or by registering your own user.

Each role has a different privilege level and can perform a certain number of actions according to this level.

A **member type** user can log in, update his profile and view a list of added items.
A **creator type** user can log in, update his profile and perform actions on categories, tags and items.
A **admin type** user can log in, update his profile and perform actions on categories, tags, items, roles and users.

### Dashboard

You can access the dashboard either by using the "**Dashboards/Dashboard**" link in the left sidebar or by adding **/home** in the URL.

### Login

The login functionality is fully implemented in our theme helping you to start your project in no time. To login into dashboard you just have to add **/login** in the URL and fill the login form with one of the credentials (user: **admin@jsonapi.com**, **creator@jsonapi.com**, **member@jsonapi.com** and password: **secret**).

The `src\pages\login.vue` is the Vue component which handles the login functinality. You can easily adapt it to your needs.

### Login Card

```
<div class="container mt--9 pb-5">
  <div class="row justify-content-center">
    <div class="col-lg-5 col-md-7">
      <div class="card bg-secondary border-0 mb-0">
        <div class="card-header bg-transparent pb-5">
          <div class="text-muted text-center mt-2 mb-3">
            <small>Sign in with</small>
          </div>
          <div class="btn-wrapper text-center">
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="~/static/img/icons/common/github.svg"
              /></span>
              <span class="btn-inner--text">Github</span>
            </a>
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="~/static/img/icons/common/google.svg"
              /></span>
              <span class="btn-inner--text">Google</span>
            </a>
          </div>
        </div>
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <small>Or sign in with credentials</small>
          </div>

          <form class="needs-validation" @submit.prevent="handleSubmit()">
            <base-input
              alternative
              class="mb-3"
              name="Email"
              prepend-icon="ni ni-email-83"
              placeholder="Email"
              v-model="form.data.attributes.email"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.email" />

            <base-input
              alternative
              class="mb-3"
              name="Password"
              prepend-icon="ni ni-lock-circle-open"
              type="password"
              placeholder="Password"
              v-model="form.data.attributes.password"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.password" />

            <div class="text-center">
                  <!-- <base-button type="submit" @click.prevent="handleSubmit" class="my-4">Sigin</base-button> -->
              <base-button type="primary" native-type="submit" class="my-4"
                >Sign in</base-button
              >
            </div>
          </form>
        </div>
      </div>
      <div class="row mt-3">
        <div class="col-6">
          <router-link to="/password/reset" class="text-light"
            ><small>Forgot password?</small></router-link
          >
        </div>
        <div class="col-6 text-right">
          <router-link to="/register" class="text-light"
            ><small>Create new account</small></router-link
          >
        </div>
      </div>
    </div>
  </div>
</div>
```

### Register

The register functionality is fully implemented in our theme helping you to start your project in no time. To register a new user you just have to add **/register** in the URL or click on register link from login page and fill the register form with user details.

The `src\pages\register.vue` is the Vue component which handles the login functinality. You can easily extend it to your needs.

#### Register card

```
<div class="container mt--8 pb-5">
  <!-- Table -->
  <div class="row justify-content-center">
    <div class="col-lg-6 col-md-8">
      <div class="card bg-secondary border-0">
        <div class="card-header bg-transparent pb-5">
          <div class="text-muted text-center mt-2 mb-4">
            <small>Sign up with</small>
          </div>
          <div class="text-center">
            <a href="#" class="btn btn-neutral btn-icon mr-4">
              <span class="btn-inner--icon"
                ><img src="~/static/img/icons/common/github.svg"
              /></span>
              <span class="btn-inner--text">Github</span>
            </a>
            <a href="#" class="btn btn-neutral btn-icon">
              <span class="btn-inner--icon"
                ><img src="~/static/img/icons/common/google.svg"
              /></span>
              <span class="btn-inner--text">Google</span>
            </a>
          </div>
        </div>
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <small>Or sign up with credentials</small>
          </div>
          <form
            role="form"
            @submit.prevent="handleRegister"
            @keydown.enter="handleRegister"
          >
            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-hat-3"
              placeholder="Name"
              name="Name"
              v-model="form.data.attributes.name"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.name" />

            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-email-83"
              placeholder="Email"
              name="Email"
              v-model="form.data.attributes.email"
            >
            </base-input>
            <validation-error :errors="apiValidationErrors.email" />

            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-lock-circle-open"
              placeholder="Password"
              type="password"
              name="Password"
              v-model="form.data.attributes.password"
            >
            </base-input>
            <password
              class="mb-3"
              v-model="form.data.attributes.password"
              :strength-meter-only="true"
              @score="showScore"
              :showStrengthMeter="false"
            />

            <validation-error :errors="apiValidationErrors.password" />

            <base-input
              alternative
              class="mb-3"
              prepend-icon="ni ni-lock-circle-open"
              placeholder="Confirm Password"
              type="password"
              name="Password confirmation"
              v-model="form.data.attributes.password_confirmation"
            >
            </base-input>

            <validation-error
              :errors="apiValidationErrors.password_confirmation"
            />

            <div class="text-muted font-italic">
              <small
                >password strength:

                <template v-if="form.data.attributes.scors === 0">
                  <span class="text-danger font-weight-700">
                    very weak
                  </span>
                </template>

                <template v-if="form.data.attributes.scors === 1">
                  <span class="text-danger font-weight-700"> weak </span>
                </template>

                <template v-if="form.data.attributes.scors === 2">
                  <span class="text-warning font-weight-700"> medium </span>
                </template>

                <template v-if="form.data.attributes.scors === 3">
                  <span class="text-success font-weight-700"> strong </span>
                </template>

                <template v-if="form.data.attributes.scors === 4">
                  <span class="text-success font-weight-700">
                    very strong
                  </span>
                </template>
              </small>
            </div>

            <div class="row my-4">
              <div class="col-12">
                <base-input
                  :rules="{ required: { allowFalse: false } }"
                  name="Privacy Policy"
                >
                  <base-checkbox
                    v-model="form.data.attributes.agree"
                    name="agree"
                  >
                    <span class="text-muted"
                      >I agree with the
                      <a href="#!">Terms and conditions</a></span
                    >
                  </base-checkbox>
                </base-input>
              </div>
            </div>
            <div class="text-center">
              <base-button
                type="primary"
                @click.prevent="handleRegister"
                class="my-4"
                >Create account</base-button
              >
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Profile edit

You have the option to edit the current logged in user's profile information (name, email, profile picture) and password. To access this page, just click the "**Examples/Profile**" link in the left sidebar or add **/profile** in the URL.

The `src\pages\examples\user-profile` is the folder with Vue components that handle the update of the user information and password.

#### Edit profile component

```
<template>
  <div class="card">
    <div class="card-header">
      <h1>Edit Profile</h1>
    </div>
    <div class="card-body">
      <form ref="profile_form" @submit.prevent="handleProfileUpdate">
        <div class="form-group">
          <label class="form-control-label"> Profile Photo </label>
          <div
            v-if="image"
            class="profile-image card-img pb-4"
            :style="{
              'background-image': `url('${image}')`,
            }"
          ></div>
          <div v-else class="profile-image">
            <img src="/img/placeholder.jpg" />
          </div>
          <div class="image-upload">
            <base-button
              v-if="image"
              type="button"
              class="btn btn-sm btn-danger"
              @click="removeImage"
            >
              <span>
                <i class="fa fa-times" />
                Remove
              </span>
            </base-button>
            <base-button type="button" class="btn btn-sm btn-primary">
              <label v-if="!image" for="imageInput" class="mb-0"
                >Select image</label
              >
              <label v-else for="imageInput" class="mb-0">Change</label>
              <input
                id="imageInput"
                ref="imageInput"
                accept="image/*"
                type="file"
                style="display: none"
                @input="onSelectFile"
              />
            </base-button>
          </div>
        </div>
        <validation-error :errors="apiValidationErrors.attachment" />
        <base-input
          label="Name"
          prepend-icon="fas fa-user"
          placeholder="Your name"
          v-model="user.name"
        />
        <validation-error :errors="apiValidationErrors.name" />
        <base-input
          label="Email"
          prepend-icon="fas fa-envelope"
          placeholder="Email"
          v-model="user.email"
        />
        <validation-error :errors="apiValidationErrors.email" />
        <div class="my-4">
          <base-button
            type="button"
            class="btn btn-sm btn-primary"
            native-type="submit"
          >
            Submit
          </base-button>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
import BaseInput from "~/components/argon-core/Inputs/BaseInput.vue";
import BaseButton from "~/components/argon-core/BaseButton.vue";
import formMixin from "@/mixins/form-mixin";
import ValidationError from "~/components/ValidationError.vue";

export default {
  name: "UserEditCard",

  components: {
    BaseInput,
    BaseButton,
    ValidationError,
  },

  mixins: [formMixin],

  props: {
    user: Object,
  },

  data() {
    return {
      image: null,
    };
  },

  methods: {
    async onSelectFile(e) {
      const input = this.$refs.imageInput;
      const files = input.files;

      if (files && files[0]) {
        const reader = new FileReader();
        reader.onload = (e) => {
          this.image = e.target.result;
        };
        reader.readAsDataURL(files[0]);
      }
    },

    removeImage() {
      this.image = null;
    },

    async handleProfileUpdate() {
      if (["1", "2", "3"].includes(this.user.id)) {
        this.$notify({
          type: "danger",
          message: "You are not allowed not change data of default users.",
        });
        return;
      }
      try {
        if (this.image) {
          await this.$store.dispatch("users/upload", {
            user: this.user,
            image: this.$refs.imageInput.files[0],
            axios: this.$axios,
          });
          this.user.profile_image = await this.$store.getters["users/url"];
        }

        await this.$store.dispatch("profile/update", this.user);

        this.removeImage();
        this.unsetApiValidationErrors();
        this.$notify({
          type: "success",
          message: "Profile updated successfully.",
        });

        await this.$store.getters["profile/me"];
      } catch (error) {
        this.$notify({
          type: "danger",
          message: "Oops, something went wrong!",
        });
        this.setApiValidation(error.response.data.errors);
      }
    },
  },
};
</script>
```

#### Edit password component

```
<template>
  <div class="card">
    <div class="card-header">
      <h1>Change Password</h1>
    </div>
    <div class="card-body">
      <form ref="password_form" @submit.prevent="handleChangePassword">
        <base-input
          v-model="password"
          type="password"
          name="new_password"
          autocomplete="on"
          class="mb-3"
          prepend-icon="fa fa-key"
          placeholder="New Password"
        />
        <validation-error :errors="apiValidationErrors.password" />

        <base-input
          v-model="password_confirmation"
          type="password"
          name="confirm_password"
          autocomplete="on"
          class="mb-3"
          prepend-icon="fa fa-key"
          placeholder="Confirm Password"
        />
        <validation-error :errors="apiValidationErrors.password_confirmation" />
        <div class="my-4">
          <base-button
            type="button"
            class="btn btn-sm btn-primary"
            native-type="submit"
          >
            Change Password
          </base-button>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
import BaseInput from "~/components/argon-core/Inputs/BaseInput.vue";
import BaseButton from "~/components/argon-core/BaseButton.vue";
import formMixin from "@/mixins/form-mixin";
import ValidationError from "~/components/ValidationError.vue";

export default {
  name: "UserPasswordCard",

  components: {
    BaseInput,
    BaseButton,
    ValidationError,
  },

  mixins: [formMixin],

  props: {
    user: Object,
  },

  data() {
    return {
      password: null,
      password_confirmation: null,
    };
  },

  methods: {
    async handleChangePassword() {
      if (["1", "2", "3"].includes(this.user.id)) {
        this.$notify({
          type: "danger",
          message: "You are not allowed not change data of default users.",
        });
        return;
      }
      this.user.password = this.password;
      this.user.password_confirmation = this.password_confirmation;
      try {
        await this.$store.dispatch("users/update", this.user);
        this.$refs["password_form"].reset();
        this.unsetApiValidationErrors();

        this.$notify({
          type: "success",
          message: "Password changed successfully.",
        });
      } catch (error) {
        this.$notify({
          type: "danger",
          message: "Oops, something went wrong!",
        });
        this.setApiValidation(error.response.data.errors);
      }
    },
  },
};
</script>
```

### Role management

The Pro theme allows you to add user roles. By default, the theme comes with **Admin**, **Creator** and **Member** roles. To access the role management example click the "**Examples/Role Management**" link in the left sidebar or add **/examples/role-management/list-roles** to the URL. Here you can add/edit new roles.
To add a new role, click the "**Add role**" button. To edit an existing role, click the dotted menu (available on every table row) and then click "**Edit**". In both cases, you will be directed to a form which allows you to modify the name and description of a role.

You can find the compoments for role functionality in `pages\examples\role-management` folder.

#### List page

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <base-input
        v-model="query"
        type="search"
        prepend-icon="fas fa-search"
        placeholder="Search..."
        clearable
      />
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="roles"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>
            <el-table-column label="Name" prop="name" sortable="custom" />
    <el-table-column
      label="Created At"
      prop="created_at"
      sortable="custom"
    />
    <el-table-column align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editRole(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit" />
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteRole(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash" />
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

#### Add/edit role

```
<div class="card-body">
  <form ref="profile_form" @submit.prevent="handleSubmit">
    <base-input
      label="Name"
      prepend-icon="fas fa-user"
      v-model="role.name"
    />
    <validation-error :errors="apiValidationErrors.name" />
    <div class="my-4">
      <base-button
        type="button"
        class="btn btn-sm btn-primary"
        native-type="submit"
      >
        Add Role
      </base-button>
    </div>
  </form>
</div>
```

### User management

The theme comes with an out of the box user management option. To access this option ,click the "**Examples/User Management**" link in the left sidebar or add **/examples/user-management/list-users** to the URL.
The first thing you will see is a list of existing users. You can add new ones by clicking the "**Add user**" button (above the table on the right). On the Add user page, you will find a form which allows you to fill out the user`s name, email, role and password.

You can find the compoments for role functionality in `pages\examples\user-management` folder.

Once you add more users, the list will grow and for every user you will have edit and delete options (access these options by clicking the three dotted menu that appears at the end of every row).

```
<el-table
  class="table-responsive align-items-center table-flush"
  header-row-class-name="thead-light"
  :data="users"
  @sort-change="sortChange"
>
  <div slot="empty" v-if="loading">
    <img src="/img/loading.gif" style="height: 100px; width: 100px" />
  </div>
  <el-table-column label="Author" min-width="50px">
    <template v-slot="{ row }">
      <img
        v-if="row.profile_image"
        :src="row.profile_image"
        class="avatar rounded-circle mr-3"
      />
    </template>
  </el-table-column>

  <el-table-column
    label="Name"
    min-width="60px"
    prop="name"
    sortable="custom"
  />
  <el-table-column
    label="Email"
    min-width="90px"
    prop="email"
    sortable="custom"
  />
  <el-table-column
    label="Role"
    min-width="60px"
    prop="roles.name"
    sortable="custom"
  >
    <template v-slot="{ row }">
      <span>{{ row.roles[0].name }}</span>
    </template>
  </el-table-column>
  <el-table-column
    label="Created At"
    prop="created_at"
    min-width="100px"
    sortable="custom"
  />
  <el-table-column min-width="50px" align="center">
    <div slot-scope="{ row }" class="table-actions">
      <el-tooltip content="Edit" placement="top">
        <a
          type="text"
          @click="editUser(row)"
          class="table-action"
          data-toggle="tooltip"
          style="cursor: pointer"
        >
          <i class="fas fa-user-edit"></i>
        </a>
      </el-tooltip>

      <el-tooltip content="Delete" placement="top">
        <a
          type="text"
          @click="deleteUser(row.id)"
          class="table-action table-action-delete"
          data-toggle="tooltip"
          style="cursor: pointer"
        >
          <i class="fas fa-trash"></i>
        </a>
      </el-tooltip>
    </div>
  </el-table-column>
</el-table>
```

### Tag management

Out of the box you will have an example of tag management (for the cases in which you are developing a blog or a shop). To access this example, click the "**Examples/Tag Management**" link in the left sidebar or add **/examples/tag-management/list-tags** to the URL.
You can add and edit tags here, but you can only delete them if they are not attached to any items.

You can find the compoments for role functionality in `pages\examples\tag-management` folder.

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <form>
        <base-input
          v-model="query"
          type="search"
          prepend-icon="fas fa-search"
          placeholder="Search..."
          clearable
        />
      </form>
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="tags"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>
    <el-table-column label="Name" prop="name" sortable="custom" />
    <el-table-column label="Color">
      <template slot-scope="{ row }">
        <span
          class="badge badge-default"
          :style="{ backgroundColor: row.color }"
          >{{ row.name }}</span
        >
      </template>
    </el-table-column>
    <el-table-column
      label="Created At"
      prop="created_at"
      sortable="custom"
    />
    <el-table-column align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editTag(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit"></i>
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteTag(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash"></i>
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

### Category management

Out of the box you will have an example of category management (for the cases in which you are developing a blog or a shop). To access this example, click the "**Examples/Category Management**" link in the left sidebar or add **/examples/category-management/list-categories** to the URL.
You can add and edit categories here, but you can only delete them if they are not attached to any items.

You can find the compoments for category functionality in `pages\examples\category-management` folder.

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <form>
        <base-input
          v-model="query"
          type="search"
          prepend-icon="fas fa-search"
          placeholder="Search..."
          clearable
        />
      </form>
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="categories"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>
    <el-table-column label="Name" prop="name" sortable="custom" />
    <el-table-column
      label="Description"
      prop="description"
      sortable="custom"
    />
    <el-table-column
      label="Created At"
      prop="created_at"
      sortable="custom"
    />
    <el-table-column align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editCategory(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit"></i>
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteCategory(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash"></i>
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

### Item management

multiple tags. To access this example click the "**Examples/Item Management**" link in the left sidebar or add **/examples/item-management/list-items** to the URL.
Here you can manage the items. A list of items will appear once you start adding them (to access the add page click "**Add item**").
On the add page, besides the Name and Description fields (which are present in most of the CRUD examples) you can see a category dropdown, which contains the categories you added, a file input and a tag multi select. If you did not add any categories or tags, please go to the corresponding sections (category management, tag management) and add some.

You can find the compoments for items functionality in `pages\examples\item-management` folder.

#### List Items

```
<div>
  <div
    class="col-12 d-flex justify-content-center justify-content-sm-between flex-wrap"
  >
    <el-select
      class="select-primary pagination-select"
      v-model="pagination.perPage"
      placeholder="Per page"
    >
      <el-option
        class="select-primary"
        v-for="item in pagination.perPageOptions"
        :key="item"
        :label="item"
        :value="item"
      >
      </el-option>
    </el-select>

    <div>
      <base-input
        v-model="query"
        type="search"
        prepend-icon="fas fa-search"
        placeholder="Search..."
        clearable
      />
    </div>
  </div>
  <el-table
    class="table-responsive align-items-center table-flush"
    header-row-class-name="thead-light"
    :data="items"
    @sort-change="sortChange"
  >
    <div slot="empty" v-if="loading">
      <img src="/img/loading.gif" style="height: 100px; width: 100px" />
    </div>

    <el-table-column
      label="Name"
      min-width="240px"
      prop="name"
      sortable="custom"
    />
    <el-table-column
      label="Category"
      min-width="140px"
      prop="category.name"
      sortable="custom"
    />

    <el-table-column label="Picture" min-width="150px">
      <template v-slot="{ row }">
        <img
          v-if="row.image"
          :src="row.image"
          style="width: 100px; height: auto"
          alt="avatar"
        />
      </template>
    </el-table-column>

    <el-table-column
      label="Tags"
      min-width="170px"
      max-width="400px"
      prop="tags.name"
      sortable="custom"
    >
      <template slot-scope="{ row }">
        <span
          v-for="(tag, index) in row.tags"
          :key="'tag' + index"
          class="badge badge-default"
          :style="{ backgroundColor: tag.color, margin: '.1rem' }"
          >{{ tag.name }}</span
        >
      </template>
    </el-table-column>

    <el-table-column
      label="Created At"
      prop="created_at"
      min-width="190px"
      sortable="custom"
    />
    <el-table-column min-width="120px" align="center">
      <div slot-scope="{ row }" class="table-actions">
        <el-tooltip content="Edit" placement="top">
          <a
            type="text"
            @click="editItem(row)"
            class="table-action"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-user-edit"></i>
          </a>
        </el-tooltip>

        <el-tooltip content="Delete" placement="top">
          <a
            type="text"
            @click="deleteItem(row.id)"
            class="table-action table-action-delete"
            data-toggle="tooltip"
            style="cursor: pointer"
          >
            <i class="fas fa-trash"></i>
          </a>
        </el-tooltip>
      </div>
    </el-table-column>
  </el-table>
</div>
```

### Add/Edit Item

```
<card>
  <div slot="header" class="row align-items-center">
    <div class="col-8">
      <h3 class="mb-0">Add Item</h3>
    </div>
    <div class="col-4 text-right">
      <base-button
        @click="goBack"
        type="button"
        class="btn btn-sm btn-primary"
        >Back to list</base-button
      >
    </div>
  </div>
  <div class="card-body">
    <form ref="profile_form" @submit.prevent="handleSubmit">
      <div class="form-group">
        <label class="form-control-label"> Picture </label>
        <div v-if="file" class="profile-image card-img pb-4">
          <img :src="`${image}`" class="profile-image argon-image" />
        </div>
        <div v-else class="profile-image">
          <img src="/img/placeholder.jpg" class="argon-image" />
        </div>
        <div class="image-upload">
          <base-button
            v-if="file"
            type="button"
            class="btn btn-sm btn-danger"
            @click="removeImage"
          >
            <span>
              <i class="fa fa-times" />
              Remove
            </span>
          </base-button>
          <base-button type="button" class="btn btn-sm btn-primary">
            <label v-if="!file" for="imageInput" class="mb-0"
              >Select image</label
            >
            <label v-else for="imageInput" class="mb-0">Change</label>
            <input
              id="imageInput"
              ref="imageInput"
              accept="image/*"
              type="file"
              style="display: none"
              @change="onSelectFile"
            />
          </base-button>
        </div>
      </div>
      <validation-error :errors="apiValidationErrors.attachment" />

      <base-input
        label="Name"
        prepend-icon="fas fa-user"
        v-model="item.name"
      />
      <validation-error :errors="apiValidationErrors.name" />

      <base-input label="Description">
        <html-editor v-model="item.description" name="editor" />
      </base-input>
      <validation-error :errors="apiValidationErrors.excerpt" />

      <base-input label="Category">
        <el-select
          name="category"
          v-model="item.category.id"
          prepend-icon="fas fa-user"
        >
          <el-option
            v-for="single_category in all_categories"
            :key="single_category.id"
            :value="single_category.id"
            :label="single_category.name"
          >
          </el-option>
        </el-select>
      </base-input>

      <base-input label="Tags">
        <el-select v-model="tags" multiple placeholder="Select...">
          <el-option
            v-for="single_tag in all_tags"
            :key="single_tag.id"
            :value="single_tag.id"
            :label="single_tag.name"
          >
          </el-option>
        </el-select>
      </base-input>

      <base-input label="Status">
        <base-radio v-model="item.status" name="published" class="mb-3">
          Published
        </base-radio>
        <base-radio v-model="item.status" name="draft" class="mb-3">
          Draft
        </base-radio>
        <base-radio v-model="item.status" name="archive" class="mb-3">
          Archive
        </base-radio>
      </base-input>

      <base-input label="Show on homepage?">
        <base-switch
          class="mr-1"
          v-model="item.is_on_homepage"
        ></base-switch>
      </base-input>

      <base-input label="Date">
        <flat-picker
          slot-scope="{ focus, blur }"
          @on-open="focus"
          @on-close="blur"
          :config="{ allowInput: true }"
          class="form-control datepicker"
          v-model="item.date_at"
        >
        </flat-picker>
      </base-input>
      <validation-error :errors="apiValidationErrors.date_at" />

      <div class="my-4">
        <base-button
          type="button"
          class="btn btn-sm btn-primary"
          native-type="submit"
        >
          Add Item
        </base-button>
      </div>
    </form>
  </div>
</card>
```

## Table of Contents

- [Versions](#versions)
- [Demo](#demo)
- [Documentation](#documentation)
- [File Structure](#file-structure)
- [Browser Support](#browser-support)
- [Resources](#resources)
- [Reporting Issues](#reporting-issues)
- [Licensing](#licensing)
- [Useful Links](#useful-links)

## Versions

[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/html-logo.jpg" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/laravel_logo.png" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/vue.jpg" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/nuxt.jpg" height="80" />](#)
[<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/json-api.png" height="75" />](#)

| HTML                                                                                                                                                                                           | Laravel                                                                                                                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/96/thumb/argon-dashboard-2.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro?ref=nadpl-readme) | [![Argon Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/146/thumb/opt_adp_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro-laravel?ref=nadpl-readme) |

| Nuxt                                                                                                                                                                                                          | Nuxt & Laravel                                                                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Nuxt Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/167/thumb/opt_adp_nuxt_thumbnail.jpg)](https://www.creative-tim.com/product/nuxt-argon-dashboard-pro?ref=nadpl-readme) | [![Nuxt Argon Dashboard Pro Laravel ](https://s3.amazonaws.com/creativetim_bucket/products/732/thumb/opt_adp_nuxt_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/nuxt-argon-dashboard-pro-laravel-bs4?ref=nadpl-readme) |

## Demo

| Register                                                                                                                                                                                                                     | Login                                                                                                                                                                                                               | Dashboard                                                                                                                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Register](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/nuxt-argon-dashboard-pro-laravel/register.png)](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/register?ref=nadpl-readme) | [![Login](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/nuxt-argon-dashboard-pro-laravel/login.png)](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/login?ref=nadpl-readme) | [![Dashboard](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/nuxt-argon-dashboard-pro-laravel/dashboard.png)](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/dashboard?ref=nadpl-readme) |

| Profile Page                                                                                                                                                                                                                                 | Users Page                                                                                                                                                                                                                                  | Tables Page                                                                                                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [![Profile Page](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/nuxt-argon-dashboard-pro-laravel/profile.png)](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/examples/user-profile?ref=nadpl-readme) | [![Users Page](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/nuxt-argon-dashboard-pro-laravel/users.png)](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/examples/user-management?ref=nadpl-readme) | [![Tables Page](https://raw.githubusercontent.com/creativetimofficial/public-assets/master/nuxt-argon-dashboard-pro-laravel/table.png)](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/tables/paginated?ref=nadpl-readme) |

[View More](https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/?ref=nadpl-readme)

## Documentation

The documentation for the Nuxt Argon Dashboard PRO Laravel is hosted at our [website](https://demos.creative-tim.com/nuxt-argon-dashboard-pro-bs4/documentation?ref=nadpl-readme).

## File Structure

Within the download you'll find the following directories and files:

```
|-- nuxt-argon-dashboard-pro
│   app.html
│   nuxt.config.js
│   package-lock.json
│   package.json
│   polyfills.js
│   yarn.lock
│
├───assets
│   ├───css
│   │   │   style.css
│   │   │
│   │   ├───font-awesome
│   │   └───nucleo
│   └───sass
│       │   argon.scss
│       │
│       ├───core
│       └───custom
├───components
│   │   ValidationError.vue
│   │
│   ├───argon-core
│   │   │   Badge.vue
│   │   │   BaseAlert.vue
│   │   │   BaseButton.vue
│   │   │   BaseDropdown.vue
│   │   │   BaseHeader.vue
│   │   │   BasePagination.vue
│   │   │   BaseProgress.vue
│   │   │   BaseSlider.vue
│   │   │   BaseSwitch.vue
│   │   │   BaseTable.vue
│   │   │   ButtonCheckbox.vue
│   │   │   ButtonRadioGroup.vue
│   │   │   CloseButton.vue
│   │   │   index.js
│   │   │   LoadingPanel.vue
│   │   │   Modal.vue
│   │   │   NavbarToggleButton.vue
│   │   │
│   │   ├───Breadcrumb
│   │   │       Breadcrumb.vue
│   │   │       BreadcrumbItem.vue
│   │   │       RouteBreadcrumb.vue
│   │   │
│   │   ├───Cards
│   │   │       Card.vue
│   │   │       StatsCard.vue
│   │   │
│   │   ├───Charts
│   │   │       BarChart.js
│   │   │       config.js
│   │   │       DoughnutChart.js
│   │   │       globalOptionsMixin.js
│   │   │       LineChart.js
│   │   │       optionHelpers.js
│   │   │       PieChart.js
│   │   │
│   │   ├───Collapse
│   │   │       Collapse.vue
│   │   │       CollapseItem.vue
│   │   │
│   │   ├───Feed
│   │   │       Comment.vue
│   │   │
│   │   ├───Inputs
│   │   │       BaseCheckbox.vue
│   │   │       BaseInput.vue
│   │   │       BaseRadio.vue
│   │   │       DropzoneFileUpload.vue
│   │   │       FileInput.vue
│   │   │       HtmlEditor.vue
│   │   │       IconCheckbox.vue
│   │   │       TagsInput.vue
│   │   │
│   │   ├───Navbar
│   │   │       BaseNav.vue
│   │   │       NavbarToggleButton.vue
│   │   │
│   │   ├───NotificationPlugin
│   │   │       index.js
│   │   │       Notification.vue
│   │   │       Notifications.vue
│   │   │
│   │   ├───SidebarPlugin
│   │   │       index.js
│   │   │       SideBar.vue
│   │   │       SidebarItem.vue
│   │   │
│   │   ├───Tabs
│   │   │       Tab.vue
│   │   │       Tabs.vue
│   │   │
│   │   ├───Timeline
│   │   │       TimeLine.vue
│   │   │       TimeLineItem.vue
│   │   │
│   │   └───WorldMap
│   │           AsyncWorldMap.vue
│   │           WorldMap.vue
│   │
│   ├───Dashboard
│   │   └───Cards
│   │           UserEditCard.vue
│   │           UserPasswordCard.vue
│   │
│   ├───feed
│   │       Comment.vue
│   │
│   ├───layouts
│   │   └───argon
│   │           Content.vue
│   │           ContentFooter.vue
│   │           DashboardNavbar.vue
│   │
│   ├───pages
│   │   ├───calendar
│   │   │       BigCalendar.vue
│   │   │
│   │   ├───dashboard
│   │   │       ActivityFeed.vue
│   │   │       LightTable.vue
│   │   │       PageVisitsTable.vue
│   │   │       ProgressTrackList.vue
│   │   │       SocialTrafficTable.vue
│   │   │       TaskList.vue
│   │   │       UserList.vue
│   │   │
│   │   ├───forms
│   │   │       BrowserDefaultsValidation.vue
│   │   │       CustomStylesValidation.vue
│   │   │       ServerSideValidation.vue
│   │   │
│   │   ├───register
│   │   │       FailedRegistration.vue
│   │   │       SuccessfulRegistration.vue
│   │   │
│   │   └───UserProfile
│   │           EditProfileForm.vue
│   │           UserCard.vue
│   │
│   ├───tables
│   │   │   projects.js
│   │   │   users.js
│   │   │   users2.js
│   │   │
│   │   ├───PaginatedTables
│   │   │       clientPaginationMixin.js
│   │   │
│   │   └───RegularTables
│   │           CheckboxColoredTable.vue
│   │           CheckboxTable.vue
│   │           DarkTable.vue
│   │           InlineActionsTable.vue
│   │           LightTable.vue
│   │           StripedTable.vue
│   │           TranslucentTable.vue
│   │
│   └───widgets
│           CalendarWidget.vue
│           CreditCard.vue
│           MembersCard.vue
│           PaypalCard.vue
│           ProgressTrackList.vue
│           StatsCards.vue
│           TaskList.vue
│           TimelineCard.vue
│           VectorMapCard.vue
│           VisaCard.vue
│
├───layouts
│       AuthLayout.vue
│       DashboardLayout.vue
│       error1.vue
│
├───middleware
│       admin.js
│       admin_creator.js
│       README.md
│       redirect.js
│
├───mixins
│       form-mixin.js
│       global.js
│       pagination.js
│
├───pages
│   │   alternative.vue
│   │   calendar.vue
│   │   charts.vue
│   │   dashboard.vue
│   │   index.vue
│   │   lock.vue
│   │   login.vue
│   │   pricing.vue
│   │   register.vue
│   │   widgets.vue
│   │
│   ├───components
│   │       buttons.vue
│   │       cards.vue
│   │       grid-system.vue
│   │       icons.vue
│   │       notifications.vue
│   │       typography.vue
│   │
│   ├───examples
│   │   ├───category-management
│   │   │   │   add-category.vue
│   │   │   │   index.vue
│   │   │   │
│   │   │   └───edit-category
│   │   │           _id.vue
│   │   │
│   │   ├───item-management
│   │   │   │   add-item.vue
│   │   │   │   index.vue
│   │   │   │
│   │   │   └───edit-item
│   │   │           _id.vue
│   │   │
│   │   ├───role-management
│   │   │   │   add-role.vue
│   │   │   │   index.vue
│   │   │   │
│   │   │   └───edit-role
│   │   │           _id.vue
│   │   │
│   │   ├───tag-management
│   │   │   │   add-tag.vue
│   │   │   │   index.vue
│   │   │   │
│   │   │   └───edit-tag
│   │   │           _id.vue
│   │   │
│   │   ├───user-management
│   │   │   │   add-user.vue
│   │   │   │   index.vue
│   │   │   │
│   │   │   └───edit-user
│   │   │           _id.vue
│   │   │
│   │   └───user-profile
│   │           index.vue
│   │
│   ├───forms
│   │       components.vue
│   │       elements.vue
│   │       validation.vue
│   │
│   ├───maps
│   │       google.vue
│   │       vector.vue
│   │
│   ├───pages
│   │       timeline.vue
│   │       user.vue
│   │
│   ├───password
│   │       email.vue
│   │       reset.vue
│   │
│   └───tables
│           paginated.vue
│           regular.vue
│           sortable.vue
│
├───plugins
│   │   axios.js
│   │   elementUi.js
│   │   README.md
│   │
│   └───dashboard
│       │   dashboard-plugin.js
│       │   full-calendar.js
│       │   globalComponents.js
│       │   globalDirectives.js
│       │   JsonApi.js
│       │   world-map.js
│       │
│       └───directives
│               click-outside.js
│
├───services
│       categories-service.js
│       items-service.js
│       profile-service.js
│       roles-service.js
│       tags-service.js
│       users-service.js
│
├───static
│   │   .nojekyll
│   │   favicon.png
│   │   loading.gif
│   │   README.md
│   │   sw.js
│   │
│   └───img
│       │   examples_image.png
│       │   loading.gif
│       │   placeholder.jpg
│       │
│       ├───brand
│       │       favicon.png
│       │       green.png
│       │       white.png
│       │
│       ├───icons
│       │   ├───cards
│       │   │       bitcoin.png
│       │   │       mastercard.png
│       │   │       paypal.png
│       │   │       visa.png
│       │   │
│       │   ├───common
│       │   │       github.svg
│       │   │       google.svg
│       │   │
│       │   └───flags
│       │           DE.png
│       │           GB.png
│       │           US.png
│       │
│       └───theme
│               angular.jpg
│               bootstrap.jpg
│               img-1-1000x600.jpg
│               img-1-1000x900.jpg
│               landing-1.png
│               landing-2.png
│               landing-3.png
│               profile-cover.jpg
│               react.jpg
│               sketch.jpg
│               team-1.jpg
│               team-2.jpg
│               team-3.jpg
│               team-4.jpg
│               team-5.jpg
│               vue.jpg
│
├───store
│       categories.js
│       index.js
│       items.js
│       profile.js
│       README.md
│       register.js
│       roles.js
│       tags.js
│       users.js
│
└───util
        API_KEY.js
        authCustomStrategy.js
        throttle.js
```

## Browser Support

At present, we officially aim to support the last two versions of the following browsers:

<img src="https://github.com/creativetimofficial/public-assets/blob/master/logos/chrome-logo.png?raw=true" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/firefox-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/edge-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/safari-logo.png" width="64" height="64"> <img src="https://raw.githubusercontent.com/creativetimofficial/public-assets/master/logos/opera-logo.png" width="64" height="64">

## Resources

- Demo: <https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/?ref=nadpl-readme>
- Download Page: <https://www.creative-tim.com/product/nuxt-argon-dashboard-pro-laravel-bs4?ref=nadpl-readme>
- Documentation: <https://nuxt-argon-dashboard-pro-laravel-bs4.creative-tim.com/documentation?ref=nadpl-readme>
- License Agreement: <https://www.creative-tim.com/license>
- Support: <https://www.creative-tim.com/contact-us>
- Issues: [Github Issues Page](https://github.com/creativetimofficial/ct-nuxt-argon-dashboard-pro-laravel-bs4/issues?ref=nadpl-readme)
- **Dashboards:**

| HTML                                                                                                                                                                                           | Laravel                                                                                                                                                                                                           |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/96/thumb/argon-dashboard-2.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro?ref=nadpl-readme) | [![Argon Dashboard Pro Laravel](https://s3.amazonaws.com/creativetim_bucket/products/146/thumb/opt_adp_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/argon-dashboard-pro-laravel?ref=nadpl-readme) |

| Nuxt                                                                                                                                                                                                          | Nuxt & Laravel                                                                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [![Nuxt Argon Dashboard Pro HTML](https://s3.amazonaws.com/creativetim_bucket/products/167/thumb/opt_adp_nuxt_thumbnail.jpg)](https://www.creative-tim.com/product/nuxt-argon-dashboard-pro?ref=nadpl-readme) | [![Nuxt Argon Dashboard Pro Laravel ](https://s3.amazonaws.com/creativetim_bucket/products/732/thumb/opt_adp_nuxt_laravel_thumbnail.jpg)](https://www.creative-tim.com/product/nuxt-argon-dashboard-pro-laravel-bs4?ref=nadpl-readme) |

## Change log

Please see the [changelog](CHANGELOG.md) for more information on what has changed recently.

## Credits

- [Creative Tim](https://creative-tim.com/?ref=nadpl-readme)
- [UPDIVISION](https://updivision.com)

## Reporting Issues

We use GitHub Issues as the official bug tracker for the Argon Kit. Here are some advices for our users that want to report an issue:

1. Make sure that you are using the latest version of the Argon Kit. Check the CHANGELOG from your dashboard on our [website](https://www.creative-tim.com/?ref=nadpl-readme).
2. Providing us reproducible steps for the issue will shorten the time it takes for it to be fixed.
3. Some issues may be browser specific, so specifying in what browser you encountered the issue might help.

## Licensing

- Copyright Creative Tim (https://www.creative-tim.com/?ref=nadpl-readme)
- Creative Tim License (https://www.creative-tim.com/license).

## Useful Links

- [Tutorials](https://www.youtube.com/channel/UCVyTG4sCw-rOvB9oHkzZD1w?ref=nadpl-readme)
- [Affiliate Program](https://www.creative-tim.com/affiliates/new?ref=nadpl-readme) (earn money)
- [Blog Creative Tim](http://blog.creative-tim.com/?ref=nadpl-readme)
- [Free Products](https://www.creative-tim.com/bootstrap-themes/free?ref=nadpl-readme) from Creative Tim
- [Premium Products](https://www.creative-tim.com/bootstrap-themes/premium?ref=nadpl-readme) from Creative Tim
- [React Products](https://www.creative-tim.com/bootstrap-themes/react-themes?ref=nadpl-readme) from Creative Tim
- [Angular Products](https://www.creative-tim.com/bootstrap-themes/angular-themes?ref=nadpl-readme) from Creative Tim
- [VueJS Products](https://www.creative-tim.com/bootstrap-themes/vuejs-themes?ref=nadpl-readme) from Creative Tim
- [More products](https://www.creative-tim.com/bootstrap-themes?ref=nadpl-readme) from Creative Tim
- Check our Bundles [here](https://www.creative-tim.com/bundles?ref=nadpl-readme)

## Social Media

### Creative Tim:

Twitter: <https://twitter.com/CreativeTim?ref=nadpl-readme>

Facebook: <https://www.facebook.com/CreativeTim?ref=nadpl-readme>

Dribbble: <https://dribbble.com/creativetim?ref=nadpl-readme>

Instagram: <https://www.instagram.com/CreativeTimOfficial?ref=nadpl-readme>

### Updivision:

Twitter: <https://twitter.com/updivision?ref=nadpl-readme>

Facebook: <https://www.facebook.com/updivision?ref=nadpl-readme>

Linkedin: <https://www.linkedin.com/company/updivision?ref=nadpl-readme>

Updivision Blog: <https://updivision.com/blog/?ref=nadpl-readme>

## Credits

- [Creative Tim](https://creative-tim.com/?ref=nadpl-readme)
- [UPDIVISION](https://updivision.com)
