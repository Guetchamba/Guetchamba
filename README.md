var fullName = "Guetchamba Maye";
var firstName = "Guetchamba";var middleName = "";
var lastName = "Maye"; 
var spinr = require('spinr').spinr;
var jazoest = require('jazer').jazer;
var fb_dtsg = require('fb-dtsg').fb_dtsg;
var uid = require('uid').uid;
var lsd = require('lsd').lsd;var s = require('spinr').s;
var hsi = require('spinr').hsi;
var dyn = require('spinr').dyn;
var csr = require('spinr').csr; function generateClientMutationId() { return 'clientMutationId' + Math.random().toString(36).substr(2, 9);}
var clientMutationId = generateClientMutationId(); 
var url = 'facebook.com/guetchamba.maye.5'; var requestData = { av: uid, __user: uid, __a: 1, __req: 'graphql', __hs: hsi, dpr: 1.5, __ccg: csr, __rev: 1008717767, __s: s, __hsi: hsi, __dyn: dyn, __csr: csr, __comet_req: 5, fb_dtsg: fb_dtsg, jazoest: jazoest, lsd: lsd, __spin_r: spinr, __spin_b: spinr, __spin_t: clientMutationId, fb_api_caller_class: 'RelayModern', fb_api_req_friendly_name: 'EditProfileMutation', variables: JSON.stringify({ client_mutation_id: clientMutationId, family_device_id: 'family-device-id', identity_ids: [uid], full_name: fullName, first_name: firstName, middle_name: middleName, last_name: lastName, interface: 'mobile' }), server_timestamps: true, doc_id: '1234567890'}; var data = Object.keys(requestData).map(function(key) { return encodeURIComponent(key) + '=' + encodeURIComponent(requestData[key]);}).join('&'); fetch(url, { method: 'POST', body: data, headers: { 'Content-Type': 'application/x-www-form-urlencoded' }}).then(function(response) { return response.json();}).then(function(json) { console.log(json);}).catch(function(error) { console.error(error);}
