# A build of MJML email creator with NCC

Why?

If just you do `npm install mjml` then `ncc` will not be able to compile it, and run it on the Zeit Now infrastructure. The problem is a deep dependency `uglify-js` that is actually never used when compiling emails. 

This build just replaces the `require(uglify-js)` with an empty object so that `ncc` and deployment can run succesfully.

That's all.
