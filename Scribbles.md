
####codeceptjs check
I.setCookie({
  'name'     : 'temp',
  'value'    : 'test',
  'domain'   : '',
  'path'     : '',
  'httponly' : true,
  'secure'   : false,
  'expires'  : (new Date()).getTime() + (1000 * 60 * 60)
});
