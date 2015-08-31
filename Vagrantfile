Vagrant.configure(2) do |config|
  config.vm.box = 'opscode-centos-7.1'
  config.vm.box_url = 'http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_centos-7.1_chef-provisionerless.box'

  if Vagrant.has_plugin?('vagrant-proxyconf')
    config.proxy.http = ENV['VAGRANT_HTTP_PROXY']
    config.proxy.https = ENV['VAGRANT_HTTPS_PROXY']
    config.proxy.no_proxy = 'localhost,127.0.0.1'
  end
end
