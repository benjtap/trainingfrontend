<template>
  <div id="wrapper">
      <nav class="navbar navbar-fixed-top">
          <div class="container-fluid">
              <div class="navbar-left">
                  <div class="navbar-btn">
                      <router-link to="/"><img src="/assets/images/vue-logo.png" alt="Vue.js Training Logo" class="img-fluid logo" /></router-link>
                      <button type="button" class="btn-toggle-offcanvas"><i class="lnr lnr-menu fa fa-bars"></i></button>
                  </div>
                  <a href="javascript:void(0);" class="icon-menu btn-toggle-fullwidth"><i class="fa fa-arrow-left"></i></a>
              </div>

              <div class="navbar-right">
                  <div id="navbar-menu">
                      <ul class="nav navbar-nav">
                            <li>
                              <a href="javascript:void(0);" class="right_toggle icon-menu" title="Right Menu"><i class="icon-settings"></i></a>
                            </li>
                            <li>
                                <!-- 
                                    REPLACE
                                    <router-link to="/login" class="icon-menu"><i class="icon-power"></i></router-link>
                                    WITH 
                                -->
                                <a @click.prevent="loggingOut === false && logUserOut()" href="#" class="icon-menu"><i class="icon-power"></i></a>
                            </li>
                      </ul>
                  </div>
              </div>
          </div>
      </nav>

      <div id="rightbar" class="rightbar">
          <ul class="nav nav-tabs-new">
              <li class="nav-item"><a class="nav-link active" data-toggle="tab" href="#setting">Settings</a></li>
              <li class="nav-item"><a class="nav-link" data-toggle="tab" href="#chat">Chat</a></li>
          </ul>
          <div class="tab-content">
              <div class="tab-pane active" id="setting">
                  <div class="slim_scroll">
                      <div class="card">
                          <h6>Choose Theme</h6>
                          <ul class="choose-skin list-unstyled mb-0">
                              <li data-theme="purple"><div class="purple"></div></li>
                              <li data-theme="green"><div class="green"></div></li>
                              <li data-theme="orange" class="active"><div class="orange"></div></li>
                              <li data-theme="blue"><div class="blue"></div></li>
                              <li data-theme="blush"><div class="blush"></div></li>
                              <li data-theme="cyan"><div class="cyan"></div></li>
                          </ul>
                      </div>
                      <div class="card">
                          <h6>General Settings</h6>
                          <ul class="setting-list list-unstyled mb-0">
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" />
                                      <span>Report Panel Usag</span>
                                  </label>
                              </li>
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" checked />
                                      <span>Email Redirect</span>
                                  </label>
                              </li>
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" checked />
                                      <span>Notifications</span>
                                  </label>
                              </li>
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" />
                                      <span>Auto Updates</span>
                                  </label>
                              </li>
                          </ul>
                      </div>
                      <div class="card">
                          <h6>Account Settings</h6>
                          <ul class="setting-list list-unstyled mb-0">
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" />
                                      <span>Offline</span>
                                  </label>
                              </li>
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" checked />
                                      <span>Location Permission</span>
                                  </label>
                              </li>
                              <li>
                                  <label class="fancy-checkbox">
                                      <input type="checkbox" name="checkbox" checked />
                                      <span>Notifications</span>
                                  </label>
                              </li>
                          </ul>
                      </div>
                  </div>
              </div>
              <div class="tab-pane right_chat" id="chat">
                  <div class="slim_scroll">
                      <form>
                          <div class="input-group m-b-20">
                              <div class="input-group-prepend">
                                  <span class="input-group-text"><i class="icon-magnifier"></i></span>
                              </div>
                              <input type="text" class="form-control" placeholder="Search..." />
                          </div>
                      </form>
                      <div class="card">
                          <h6>Recent</h6>
                          <ul class="right_chat list-unstyled mb-0">
                              <li class="online">
                                  <a href="javascript:void(0);">
                                      <div class="media">
                                          <img class="media-object" src="/assets/images/xs/avatar4.jpg" alt="" />
                                          <div class="media-body">
                                              <span class="name">Ava Alexander <small class="float-right">Just now</small></span>
                                              <span class="message">Lorem ipsum Veniam aliquip culpa laboris minim tempor</span>
                                              <span class="badge badge-outline status"></span>
                                          </div>
                                      </div>
                                  </a>
                              </li>
                              <li class="online">
                                  <a href="javascript:void(0);">
                                      <div class="media">
                                          <img class="media-object" src="/assets/images/xs/avatar5.jpg" alt="" />
                                          <div class="media-body">
                                              <span class="name">Debra Stewart <small class="float-right">38min ago</small></span>
                                              <span class="message">Many desktop publishing packages and web page editors</span>
                                              <span class="badge badge-outline status"></span>
                                          </div>
                                      </div>
                                  </a>
                              </li>
                              <li class="offline">
                                  <a href="javascript:void(0);">
                                      <div class="media">
                                          <img class="media-object" src="/assets/images/xs/avatar2.jpg" alt="" />
                                          <div class="media-body">
                                              <span class="name">Susie Willis <small class="float-right">2hr ago</small></span>
                                              <span class="message">Contrary to belief, Lorem Ipsum is not simply random text</span>
                                              <span class="badge badge-outline status"></span>
                                          </div>
                                      </div>
                                  </a>
                              </li>
                              <li class="offline">
                                  <a href="javascript:void(0);">
                                      <div class="media">
                                          <img class="media-object" src="/assets/images/xs/avatar1.jpg" alt="" />
                                          <div class="media-body">
                                              <span class="name">Folisise Chosielie <small class="float-right">2hr ago</small></span>
                                              <span class="message">There are many of passages of available, but the majority</span>
                                              <span class="badge badge-outline status"></span>
                                          </div>
                                      </div>
                                  </a>
                              </li>
                              <li class="online">
                                  <a href="javascript:void(0);">
                                      <div class="media">
                                          <img class="media-object" src="/assets/images/xs/avatar3.jpg" alt="" />
                                          <div class="media-body">
                                              <span class="name">Marshall Nichols <small class="float-right">1day ago</small></span>
                                              <span class="message">It is a long fact that a reader will be distracted</span>
                                              <span class="badge badge-outline status"></span>
                                          </div>
                                      </div>
                                  </a>
                              </li>
                          </ul>
                      </div>
                  </div>
              </div>
          </div>
      </div>

      <div id="left-sidebar" class="sidebar">
          <div class="navbar-brand">
              <router-link to="/"><img src="/assets/images/vue-logo.png" alt="Vue.js Training Logo" class="img-fluid logo" /><span>Vue.js Training</span></router-link>
              <button type="button" class="btn-toggle-offcanvas btn btn-sm btn-default float-right"><i class="lnr lnr-menu fa fa-chevron-circle-left"></i></button>
          </div>
          <div class="sidebar-scroll">
              <div class="user-account">
                  <div class="user_div">
                      <img src="/assets/images/user.png" class="user-photo" alt="User Profile Picture" />
                  </div>
                  <div class="dropdown">
                      <span>Welcome,</span>
                      <a href="javascript:void(0);" class="dropdown-toggle user-name" data-toggle="dropdown"><strong>Christy Wert</strong></a>
                      <ul class="dropdown-menu dropdown-menu-right account">
                            <li>
                                <a href="#"><i class="icon-user"></i>My Profile</a>
                            </li>
                            <li>
                                <a href="javascript:void(0);"><i class="icon-settings"></i>Settings</a>
                            </li>
                            <li class="divider"></li>
                            <li>
                                <!-- 
                                    REPLACE
                                    <a href="#"><i class="icon-power"></i>Logout</a> 
                                    WITH 
                                -->
                                <a @click.prevent="loggingOut === false && logUserOut()" href="#"><i class="icon-power"></i>Logout</a>
                            </li>
                      </ul>
                  </div>
              </div>
              <nav id="left-sidebar-nav" class="sidebar-nav">
                  <ul id="main-menu" class="metismenu">
                      <li class="active">
                          <router-link to="/"><i class="icon-home"></i><span>Dashboard</span></router-link>
                      </li>
                  </ul>
              </nav>
          </div>
      </div>

      <div id="main-content">
          <div class="block-header">
              <div class="row clearfix">
                  <div class="col-md-6 col-sm-12">
                      <h2>Dashboard</h2>
                  </div>
                  <div class="col-md-6 col-sm-12 text-right">
                      <ul class="breadcrumb">
                          <li class="breadcrumb-item">
                              <router-link to="/"><i class="icon-home"></i></router-link>
                          </li>
                          <li class="breadcrumb-item active">Dashboard</li>
                      </ul>
                      <a href="javascript:void(0);" class="btn btn-sm btn-primary" title="">Create New</a>
                  </div>
              </div>
          </div>

          <div class="container-fluid">
              <div class="row clearfix">
                  <div class="col-12">
                      <div class="card top_report">
                          <div class="row clearfix">
                              <div class="col-lg-3 col-md-6 col-sm-6">
                                  <div class="body">
                                      <div class="clearfix">
                                          <div class="float-left">
                                              <i class="fa fa-2x fa-dollar text-col-blue"></i>
                                          </div>
                                          <div class="number float-right text-right">
                                              <h6>Total Amount</h6>
                                              <span class="font700">${{ totalPrice }}</span>
                                          </div>
                                      </div>
                                      <div class="progress progress-xs progress-transparent custom-color-blue mb-0 mt-3">
                                          <div class="progress-bar" data-transitiongoal="87"></div>
                                      </div>
                                      <small class="text-muted">19% compared to last week</small>
                                  </div>
                              </div>
                              <div class="col-lg-3 col-md-6 col-sm-6">
                                  <div class="body">
                                      <div class="clearfix">
                                          <div class="float-left">
                                              <i class="fa fa-2x fa-bar-chart-o text-col-green"></i>
                                          </div>
                                          <div class="number float-right text-right">
                                              <h6>Total Sales</h6>
                                              <span class="font700">$500</span>
                                          </div>
                                      </div>
                                      <div class="progress progress-xs progress-transparent custom-color-green mb-0 mt-3">
                                          <div class="progress-bar" data-transitiongoal="28"></div>
                                      </div>
                                      <small class="text-muted">19% compared to last week</small>
                                  </div>
                              </div>
                              <div class="col-lg-3 col-md-6 col-sm-6">
                                  <div class="body">
                                      <div class="clearfix">
                                          <div class="float-left">
                                              <i class="fa fa-2x fa-file-text text-col-red"></i>
                                          </div>
                                          <div class="number float-right text-right">
                                              <h6>All Items</h6>
                                              <span class="font700">215</span>
                                          </div>
                                      </div>
                                      <div class="progress progress-xs progress-transparent custom-color-red mb-0 mt-3">
                                          <div class="progress-bar" data-transitiongoal="41"></div>
                                      </div>
                                      <small class="text-muted">19% compared to last week</small>
                                  </div>
                              </div>
                              <div class="col-lg-3 col-md-6 col-sm-6">
                                  <div class="body">
                                      <div class="clearfix">
                                          <div class="float-left">
                                              <i class="fa fa-2x fa-user text-col-yellow"></i>
                                          </div>
                                          <div class="number float-right text-right">
                                              <h6>All Users</h6>
                                              <span class="font700">21</span>
                                          </div>
                                      </div>
                                      <div class="progress progress-xs progress-transparent custom-color-yellow mb-0 mt-3">
                                          <div class="progress-bar" data-transitiongoal="75"></div>
                                      </div>
                                      <small class="text-muted">19% compared to last week</small>
                                  </div>
                              </div>
                          </div>
                      </div>
                  </div>
              </div>
              <div class="row clearfix">
                  <div class="col-lg-12 col-md-12 col-sm-12">
                      <div class="card">
                          <div class="header">
                              <h2>All Inventory</h2>
                          </div>
                          <div class="body">
                              <div class="table-responsive">
                                    <table class="table table-hover js-basic-example dataTable table-custom mb-0">
                                        <thead class="thead-dark">
                                            <tr>
                                                <th>Date Added</th>
                                                <th>Name</th>
                                                <th>Type</th>
                                                <th>Description</th>
                                                <th>Price</th>
                                                <th>Status</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr 
                                            v-for="(item, index) in inventories"
                                            :key="index">
                                                <td>{{ item.created_at }}</td>
                                                <td>{{ item.name }}</td>
                                                <td>{{ item.type }}</td>
                                                <td>{{ item.description }}</td>
                                                <td>${{ item.price }}</td>
                                                <td>
                                                    <span v-if="item.status == 1" class="badge badge-success">sold</span>
                                                    <span v-else class="badge badge-danger">unsold</span>
                                                </td>
                                            </tr>
                                        </tbody>
                                    </table>
                              </div>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
import useInventoryStore from '../store/inventory';
import useGeneralStore from '../store/general';
import useUserStore from '../store/user';
import { mapState, mapActions } from 'pinia';
export default {
    data: () => {
        return {
            loggingOut: false
        }
    },
    computed: {
        ...mapState(useInventoryStore, [
            'inventories'
        ]),
        ...mapState(useGeneralStore, [
            'API_URL'
        ]),
        ...mapState(useUserStore, [
            'token',
            'userIsAuth'
        ]),
        totalPrice() {
            let value = 0;
            this.inventories.forEach(item => {
                value += Number(item.price)
            });
            return value;
        }
    },
    watch: {
        userIsAuth() {
            /* 
                At this point the userIsAuth value is true.
                On successful logout, after the storeLoggedInUser
                method is called, the userIsAuth value is 
                set to false and this watch property is invoked.
                The code below will then run.
            */
            this.$router.push('/login');
        }
    },
    methods: {
        ...mapActions(useInventoryStore, [
            'storeInventories'
        ]),
        ...mapActions(useUserStore, [
            'logoutUser'
        ]),
        logUserOut() {
            const _this = this;
            _this.loggingOut = true;
            axios.post(`${_this.API_URL}logout`, {}, {
                headers: {
                    Authorization: `Bearer ${_this.token}`
                }
            }).then(RESPONSE => {
                alert(RESPONSE.data.message);
            }).catch(ERROR => {
                console.log(ERROR);
                alert(ERROR.response.data.message);
            }).then(() => {
                _this.logoutUser();
                _this.loggingOut = false;
            });
        },
        fetchInventory() {
            const _this = this;
            axios.get(`${_this.API_URL}inventories`, {
                headers: {
                    Authorization: `Bearer ${_this.token}`
                }
            }).then(RESPONSE => {
                _this.storeInventories(RESPONSE.data.inventories);
            }).catch(ERROR => {
                console.log(ERROR);
                alert(ERROR.response.data.message);
            }).then(() => {
                //
            });
        }
    },
    mounted() {
        this.fetchInventory();
    }
}
</script>

<style>

</style>