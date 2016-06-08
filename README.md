# TimerManager
Crossplatform library for simple working with timers
# Example
```c++
#include <iostream>
#include "timer_manager.hpp"

int main()
{
	timer_manager::add_timer(1000, [](const timer_manager::timer_ptr_t &timer_ptr)
	{
		std::cout << "Hello, World!" << std::endl;
	}, false);

	while (true)
	{
		if (!timer_manager::process())
			break;
	}

	return 0;
}
```
