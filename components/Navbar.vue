<template>
  <div
    className="flex items-center justify-between w-full px-5 space-x-8 h-14 py-7"
  >
    <MenuIcon />
    <a href="">
      <BranchLogo />
    </a>
    <div href="" className="items-center flex-auto hidden md:flex ">
      <SearchIcon className="w-4 h-4 mr-2 " />
      <input className="w-full p-2 placeholder-gray-200" type="text"
      placeholder="Search here" onChange={(event) =>
      console.log(event.target.value)} />
    </div>
    <NameTag fullName="Berk Akgun" role="Frontend Developer" />
  </div>
</template>

<script>
export default {}
</script>

<style></style>
