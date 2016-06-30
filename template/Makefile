MOCHA_PATH=./node_modules/.bin/_mocha
COVER_PATH=./node_modules/.bin/istanbul

init-test:
	@npm install --save-dev mocha should istanbul sinon rewire \
		proxyquire supertest

# 单元测试
test:
	@NODE_ENV=test $(MOCHA_PATH) test/**/*.spec.js

# 单元测试 watch
test-w:
	@NODE_ENV=test $(MOCHA_PATH) test/**/*.spec.js --watch

# 单元测试覆盖率
test-cov:
	@NODE_ENV=test $(COVER_PATH) cover $(MOCHA_PATH) test/**/*.spec.js

# 功能 / api 测试
test-func:
	@NODE_ENV=test $(MOCHA_PATH) test/**/*.func.js

# 功能 / api 测试覆盖率
test-func-cov:
	@NODE_ENV=test $(COVER_PATH) cover $(MOCHA_PATH) test/**/*.func.js

.PHONY: install-test-dependencies test test-w test-cover \
	test-func test-func-cov
