
comment "Exported from Arsenal by RyanMiller [AM 2]";

comment "[!] UNIT MUST BE LOCAL [!]";
if (!local this) exitWith {};

comment "Remove existing items";
removeAllWeapons this;
removeAllItems this;
removeAllAssignedItems this;
removeUniform this;
removeVest this;
removeBackpack this;
removeHeadgear this;
removeGoggles this;

comment "Add weapons";
this addWeapon "rhs_weap_M107";
this addPrimaryWeaponItem "optic_KHS_blk";
this addWeapon "hgun_Pistol_heavy_01_blk_F";
this addHandgunItem "muzzle_snds_acp";
this addHandgunItem "optic_MRD";
this addHandgunItem "11Rnd_45ACP_Mag";

comment "Add containers";
this forceAddUniform "UK3CB_BAF_U_CombatUniform_MTP_ShortSleeve";
this addVest "UK3CB_BAF_V_HiVis";

comment "Add binoculars";
this addWeapon "Rangefinder";

comment "Add items to containers";
this addItemToUniform "ACE_EarPlugs";
this addItemToUniform "ACE_EntrenchingTool";
this addItemToUniform "ItemcTabHCam";
this addItemToUniform "ACE_Flashlight_XL50";
this addItemToUniform "ACE_salineIV_500";
for "_i" from 1 to 2 do {this addItemToUniform "11Rnd_45ACP_Mag";};
for "_i" from 1 to 8 do {this addItemToVest "ACE_elasticBandage";};
for "_i" from 1 to 2 do {this addItemToVest "ACE_epinephrine";};
this addHeadgear "H_Watchcap_khk";
this addGoggles "rhsusf_shemagh2_od";

comment "Add items";
this linkItem "ItemMap";
this linkItem "ItemCompass";
this linkItem "TFAR_microdagr";
this linkItem "TFAR_anprc152";
this linkItem "ItemMicroDAGR";

comment "Set identity";
[this,"WhiteHead_11","ace_novoice"] call BIS_fnc_setIdentity;
