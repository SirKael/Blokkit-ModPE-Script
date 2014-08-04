/*
If anyone share you need to put forum link or the link of my channel of Youtube <http://www.youtube.com/elsirkael>
ElSirKael Script (C) GNC copyright
Copyright (C) <2014>  <ElSirKael>

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>
*/

/*
ElSirKael all beta no sell or post
Blokkit ModScript V1.0 Mod Script By ElSirKael
*/
 
var randomspawn=true;
var blokkitdiamond;
var blokkitglowstone;
var blokkitgold;
var blokkitgrass;
var blokkitiron;
var blokkitstone;
var blokkitwood;
var PositionX;
var PositionY;
var PositionZ;
var Px;
var Py;
var Pz;
var domado = 0;
var mob = null;
var Temp;
var ticks=20;
var sp=true;
var ticks2=40;
var Xpos=0;
var Zpos=0;
var s=1; 
var s1=1;
var Xdiff=0;
var Zdiff=0;
var sd=1

var startGame = 0;

newlevel=false;
ModPE.setItem(440,"skull_zombie", 0, "Blokkit Diamond Spawner");
ModPE.setItem(441,"ruby", 0, "Blokkit Glowstone Spawner");
ModPE.setItem(442,"saddle", 0, "Blokkit Gold Spawner");
ModPE.setItem(443,"skull_creeper", 0, "Blokkit Grass Spawner");
ModPE.setItem(444,"skull_skeleton", 0, "Blokkit Iron Spawner");
ModPE.setItem(445,"skull_steve", 0, "Blokkit Stone Spawner");
ModPE.setItem(446,"skull_wither", 0, "Blokkit Wood Spawner");
Item.addCraftRecipe(440, 1, 0, [264, 9, 0]); 
Item.addCraftRecipe(441, 1, 0, [348, 9, 0]); 
Item.addCraftRecipe(442, 1, 0, [266, 9, 0]); 
Item.addCraftRecipe(443, 1, 0, [3, 9, 0]); 
Item.addCraftRecipe(444, 1, 0, [265, 9, 0]); 
Item.addCraftRecipe(445, 1, 0, [1, 9, 0]); 
Item.addCraftRecipe(446, 1, 0, [17, 9, 0]); 
 
function newLevel()
{
clientMessage("Blokkit Mod V1 By ElSirKael");
ModPE.overrideTexture("images/font/glyph_42.png", "http://i.imgur.com/rZhXzFf.png");
ModPE.overrideTexture("images/font/glyph_43.png", "http://i.imgur.com/VwK2XdV.png");
ModPE.overrideTexture("images/font/glyph_44.png", "http://i.imgur.com/7vifL26.png");
ModPE.overrideTexture("images/font/glyph_45.png", "http://i.imgur.com/nVxASoX.png");
ModPE.overrideTexture("images/font/glyph_46.png", "http://i.imgur.com/XKHoegO.png");
ModPE.overrideTexture("images/font/glyph_47.png", "http://i.imgur.com/apI3DTJ.png");
ModPE.overrideTexture("images/font/glyph_48.png", "http://i.imgur.com/4PzxlcB.png");
ModPE.overrideTexture("images/items-opaque.png", "http://i.imgur.com/Jgm2vcK.png");
newlevel=true;
}


function addBlokkitRenderType(renderer){

var var2 = 0;
var model = renderer.getModel();

var head = model.getPart("head").clear().setTextureOffset(56, 0);
var body = model.getPart("body");
var rArm = model.getPart("rightArm");
var lArm = model.getPart("leftArm");
var rLeg = model.getPart("rightLeg");
var lLeg = model.getPart("leftLeg");

body.clear();
body.setTextureOffset(0, 0);
body.addBox(-6, 10, 0, 10, 10, 10, var2);
body.addBox(0, 15, -0.5, 1, 2, 0.5, var2);
body.addBox(-3, 15, -0.5, 1, 2, 0.5, var2);

rArm.clear();
rArm.setTextureOffset(0, 21);
rArm.addBox(10, 12, 4, 3, 5, 3, var2);

lArm.clear();
lArm.setTextureOffset(0, 21);
lArm.addBox(-14, 12, 4, 3, 5, 3, var2);

rLeg.clear();
rLeg.setTextureOffset(0, 21);
rLeg.addBox(2, 6, 4, 3, 6, 3, var2);

lLeg.clear();
lLeg.setTextureOffset(0, 21);
lLeg.addBox(-7, 6, 4, 3, 6, 3, var2);
 
}

var blokkitRenderType = Renderer.createHumanoidRenderer();
addBlokkitRenderType(blokkitRenderType);


function useItem(x,y,z,itemId,block,side)
{
if(itemId==440)
{
blokkitdiamond= Level.spawnMob(x,y+1,z,10,"images/font/glyph_42.png");   
Entity.setRenderType(blokkitdiamond,blokkitRenderType.renderType); 
Entity.setNameTag(blokkitdiamond,"Blokkit Diamond");
Entity.setHealth(blokkitdiamond, 60);
}
if(itemId==441)
{
blokkitglowstone= Level.spawnMob(x,y+1,z,10,"images/font/glyph_43.png");
Entity.setRenderType(blokkitglowstone,blokkitRenderType.renderType);   
Entity.setNameTag(blokkitglowstone,"Blokkit Glowstone");
Entity.setHealth(blokkitglowstone, 60);
}
if(itemId==442)
{
blokkitgold= Level.spawnMob(x,y+1,z,10,"images/font/glyph_44.png");  
Entity.setRenderType(blokkitgold,blokkitRenderType.renderType);  
Entity.setNameTag(blokkitgold,"Blokkit Gold");
Entity.setHealth(blokkitgold, 60);
}
if(itemId==443)
{
blokkitgrass= Level.spawnMob(x,y+1,z,10,"images/font/glyph_45.png");  
Entity.setRenderType(blokkitgrass,blokkitRenderType.renderType); 
Entity.setNameTag(blokkitgrass,"Blokkit Grass");
Entity.setHealth(blokkitgrass, 60);
}
if(itemId==444)
{
blokkitiron= Level.spawnMob(x,y+1,z,10,"images/font/glyph_46.png");   
Entity.setRenderType(blokkitiron,blokkitRenderType.renderType); 
Entity.setNameTag(blokkitiron,"Blokkit Iron");
Entity.setHealth(blokkitiron, 60);
}
if(itemId==445)
{
blokkitstone= Level.spawnMob(x,y+1,z,10,"images/font/glyph_47.png"); 
Entity.setRenderType(blokkitstone,blokkitRenderType.renderType);   
Entity.setNameTag(blokkitstone,"Blokkit Stone");
Entity.setHealth(blokkitstone, 60);
}
if(itemId==446)
{
blokkitwood= Level.spawnMob(x,y+1,z,10,"images/font/glyph_48.png");   
Entity.setRenderType(blokkitwood,blokkitRenderType.renderType); 
Entity.setNameTag(blokkitwood,"Blokkit Wood");
Entity.setHealth(blokkitwood, 60);
}
}
 
function deathHook(murderer, victim)
{
if(victim==blokkitdiamond){
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 264, 3, 0);
}
else if(victim==blokkitglowstone)
{
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 348, 3, 0);
}
else if(victim==blokkitgold)
{
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 266, 3, 0);
}
else if(victim==blokkitgrass)
{
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 2, 3, 0);
}
else if(victim==blokkitiron)
{
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 265, 3, 0);
}
else if(victim==blokkitstone)
{
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 1, 3, 0);
}
else if(victim==blokkitwood)
{
Level.dropItem(Entity.getX(victim), Entity.getY(victim), Entity.getZ(victim), 0, 17, 3, 0);
}
}

function attackHook(attacker, victim)
{
if(getCarriedItem()==280)
{
  if(domado==0)
  {
    PositionX = getPlayerX();
    PositionY = getPlayerY();
    PositionZ = getPlayerZ();
    print("Mob Domado")
    mob = victim;
    domado = 1
  }
else
if(domado==1)
{
  domado = 2
}
else
if(domado==2)
{
  domado = 1
}
preventDefault();
}
}

function Tpmob(x,y,z)
{
	setPosition(mob,x,y-1,z);
	PositionX = x;
	PositionY = y;
	PositionZ = z;
}
 
function modTick()
{
if(domado==1)
{
  Temp = getPlayerX() - PositionX;
  if(Temp < 0) {Temp = -Temp;}
  if(Temp > 10) {Tpmob(getPlayerX(), getPlayerY(), getPlayerZ());}
  else
  {
  Temp = getPlayerY() - PositionY;
  if(Temp < 0) {Temp = -Temp;}
  if(Temp > 10) {Tpmob(getPlayerX(), getPlayerY(), getPlayerZ());}
  else
  {
  Temp = getPlayerZ() - PositionZ;
  if(Temp < 0) {Temp = -Temp;}
  if(Temp > 10) {Tpmob(getPlayerX(), getPlayerY(), getPlayerZ());}
  }
  }
}
else
if(domado==2)
{
  Px = getPlayerX();
  Py = getPlayerY();
  Pz = getPlayerZ();
  
  setPosition(mob,Px,Py+0.5,Pz)
}
}


function procCmd(c)
{
var cmd = c.split(" ");
if(cmd[0] == "blokkit")
{
Player.addItemInventory(440,1);
Player.addItemInventory(441,1);
Player.addItemInventory(442,1);
Player.addItemInventory(443,1);
Player.addItemInventory(444,1);
Player.addItemInventory(445,1);
Player.addItemInventory(446,1);
clientMessage("Tienes todos los spawners");
}
}
 
function leaveGame()
{
newlevel=false;
ModPE.resetImages();
}
{
startGame = 0;
}
