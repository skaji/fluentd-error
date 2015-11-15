# fluentd error

When shutting down fluentd, I encountered the following error:
```
2015-11-15 11:48:30 +0000 [info]: shutting down fluentd
2015-11-15 11:48:30 +0000 [info]: shutting down input type="forward" plugin_id="object:3fe6b4520550"
2015-11-15 11:48:30 +0000 [error]: unexpected error error=#<ArgumentError: expected loop to be an instance of Coolio::Loop> error_class=ArgumentError
2015-11-15 11:48:30 +0000 [error]: self dump: #<Fluent::ForwardInput:0x007fcd68a40aa0 @log_level=nil, @port=10001, @bind="0.0.0.0", @backlog=nil, @linger_timeout=0, @blocking_timeout=0.5, @chunk_size_warn_limit=nil, @chunk_size_limit=nil, @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @router=#<Fluent::EventRouter:0x007fcd68a45c80 @match_rules=[#<Fluent::EventRouter::Rule:0x007fcd68a411f8 @pattern=#<Fluent::AllMatchPattern:0x007fcd68a410e0>, @pattern_str="**", @collector=#<Fluent::NullOutput:0x007fcd68a421e8 @log_level=nil, @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @router=#<Fluent::EventRouter:0x007fcd68a45c80 ...>, @id=nil, @config=name:match, arg:**, {"@type"=>"null"}, [], @config_root_section=<Fluent::Config::Section {"log_level":null}>>>], @match_cache=#<Fluent::EventRouter::MatchCache:0x007fcd68a45e88 @map={"hoge"=>#<Fluent::NullOutput:0x007fcd68a421e8 @log_level=nil, @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @router=#<Fluent::EventRouter:0x007fcd68a45c80 ...>, @id=nil, @config=name:match, arg:**, {"@type"=>"null"}, [], @config_root_section=<Fluent::Config::Section {"log_level":null}>>, "fluent.warn"=>#<Fluent::NullOutput:0x007fcd68a421e8 @log_level=nil, @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @router=#<Fluent::EventRouter:0x007fcd68a45c80 ...>, @id=nil, @config=name:match, arg:**, {"@type"=>"null"}, [], @config_root_section=<Fluent::Config::Section {"log_level":null}>>}, @keys=["hoge", "fluent.warn"]>, @default_collector=#<Fluent::Agent::NoMatchMatch:0x007fcd68a45a50 @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @count=0>, @emit_error_handler=#<Fluent::RootAgent:0x007fcd68a446f0 @context=nil, @outputs=[#<Fluent::NullOutput:0x007fcd68a421e8 @log_level=nil, @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @router=#<Fluent::EventRouter:0x007fcd68a45c80 ...>, @id=nil, @config=name:match, arg:**, {"@type"=>"null"}, [], @config_root_section=<Fluent::Config::Section {"log_level":null}>>], @filters=[], @started_outputs=[#<Fluent::NullOutput:0x007fcd68a421e8 @log_level=nil, @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @router=#<Fluent::EventRouter:0x007fcd68a45c80 ...>, @id=nil, @config=name:match, arg:**, {"@type"=>"null"}, [], @config_root_section=<Fluent::Config::Section {"log_level":null}>>], @started_filters=[], @log=#<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, @event_router=#<Fluent::EventRouter:0x007fcd68a45c80 ...>, @error_collector=nil, @labels={}, @inputs=[#<Fluent::ForwardInput:0x007fcd68a40aa0 ...>], @started_inputs=[#<Fluent::ForwardInput:0x007fcd68a40aa0 ...>], @suppress_emit_error_log_interval=0, @next_emit_error_log_time=1447588107, @config=name:ROOT, arg:, {}, [name:source, arg:, {"@type"=>"forward", "port"=>"10001"}, [], name:match, arg:**, {"@type"=>"null"}, []], @config_root_section=<Fluent::Config::Section {}>>, @chain=#<Fluent::NullOutputChain:0x007fcd68a47620>>, @id=nil, @config=name:source, arg:, {"@type"=>"forward", "port"=>"10001"}, [], @config_root_section=<Fluent::Config::Section {"log_level":null,"port":10001,"bind":"0.0.0.0","backlog":null,"linger_timeout":0,"blocking_timeout":0.5,"chunk_size_warn_limit":null,"chunk_size_limit":null}>, @loop=#<Coolio::Loop:0x007fcd68a3b050 @watchers={}, @active_watchers=0, @loop=nil, @running=false>, @lsock=#<Coolio::TCPServer:0x007fcd68a3aab0 @block=nil, @args=[0, #<Fluent::Log:0x007fcd6823dc18 @out=#<IO:<STDOUT>>, @level=2, @debug_mode=false, @self_event=true, @tag="fluent", @time_format="%Y-%m-%d %H:%M:%S %z ", @depth_offset=1, @color_trace="", @color_debug="", @color_info="", @color_warn="", @color_error="", @color_fatal="", @color_reset="", @threads_exclude_events=[#<Thread:0x007fcd682fdb30@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/engine.rb:151 sleep>], @suppress_repeated_stacktrace=true>, #<Method: Fluent::ForwardInput#on_message>], @klass=Fluent::ForwardInput::Handler, @listen_socket=#<TCPServer:fd 8>>, @usock=#<UDPSocket:(closed)>, @hbr=#<Fluent::ForwardInput::HeartbeatRequestHandler:0x007fcd682fe288 @_io=#<UDPSocket:(closed)>, @_write_buffer=#<IO::Buffer:0x007fcd682fe260>, @_read_watcher=#<Coolio::IO::Watcher:0x007fcd682fe238 @coolio_io=#<Fluent::ForwardInput::HeartbeatRequestHandler:0x007fcd682fe288 ...>>, @_write_watcher=#<Coolio::IO::Watcher:0x007fcd682fe120 @coolio_io=#<Fluent::ForwardInput::HeartbeatRequestHandler:0x007fcd682fe288 ...>>, @io=#<UDPSocket:(closed)>, @callback=#<Method: Fluent::ForwardInput#on_heartbeat_request>>, @thread=#<Thread:0x007fcd682fde78@/home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/plugin/in_forward.rb:90 run>>
2015-11-15 11:48:30 +0000 [error]: loop dump: #<Coolio::Loop:0x007fcd68a3b050 @watchers={}, @active_watchers=0, @loop=nil, @running=false>
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/io.rb:35:in `attach'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/io.rb:35:in `attach'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/socket.rb:38:in `attach'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/server.rb:40:in `on_connection'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/listener.rb:45:in `on_readable'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/loop.rb:88:in `run_once'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/gems/cool.io-1.4.1/lib/cool.io/loop.rb:88:in `run'
  2015-11-15 11:48:30 +0000 [error]: /home/app/vendor/bundle/ruby/2.2.0/bundler/gems/fluentd-d5742bae0319/lib/fluent/plugin/in_forward.rb:91:in `run'
```
See [log/fluentd-only-error.log](log/fluentd-only-error.log).

Please note that fluentd here is patched so that it dumps self object when error occurs.
https://github.com/shoichikaji/fluentd/commit/d5742b

This repository reproduces the error.

## Environment

* linux (centos 6.5)
* ruby 2.2.3
* fluentd 0.12.17
* cool.io 1.4.1

```
|--fluentd -----------|     |-- fluentd in question -|
|       (out_forward) | --> | (in_forward)           |
|---------------------|     |------------------------|
```

## How to reproduce

```
$ git clone git://github.com/shoichikaji/fluentd-error.git
$ cd fluentd-error
$ docker build -t fluentd-error .

# because erros rarely occur, so run many dockers :-)
$ docker run fluentd-error 2>&1 | tee -a fluentd.log1 | grep error &
$ docker run fluentd-error 2>&1 | tee -a fluentd.log2 | grep error &
$ docker run fluentd-error 2>&1 | tee -a fluentd.log3 | grep error &
$ docker run fluentd-error 2>&1 | tee -a fluentd.log4 | grep error &
```

Wait 2~6 hours (!!!), then you will see errors.

