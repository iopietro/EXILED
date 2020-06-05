<a name='assembly'></a>
# Exiled.API

## Contents

- [AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType')
  - [Nato556](#F-Exiled-API-Enums-AmmoType-Nato556 'Exiled.API.Enums.AmmoType.Nato556')
  - [Nato762](#F-Exiled-API-Enums-AmmoType-Nato762 'Exiled.API.Enums.AmmoType.Nato762')
  - [Nato9](#F-Exiled-API-Enums-AmmoType-Nato9 'Exiled.API.Enums.AmmoType.Nato9')
- [AuthenticationType](#T-Exiled-API-Enums-AuthenticationType 'Exiled.API.Enums.AuthenticationType')
  - [Discord](#F-Exiled-API-Enums-AuthenticationType-Discord 'Exiled.API.Enums.AuthenticationType.Discord')
  - [Northwood](#F-Exiled-API-Enums-AuthenticationType-Northwood 'Exiled.API.Enums.AuthenticationType.Northwood')
  - [Patreon](#F-Exiled-API-Enums-AuthenticationType-Patreon 'Exiled.API.Enums.AuthenticationType.Patreon')
  - [Steam](#F-Exiled-API-Enums-AuthenticationType-Steam 'Exiled.API.Enums.AuthenticationType.Steam')
  - [Unknown](#F-Exiled-API-Enums-AuthenticationType-Unknown 'Exiled.API.Enums.AuthenticationType.Unknown')
- [Badge](#T-Exiled-API-Features-Badge 'Exiled.API.Features.Badge')
  - [#ctor(text,color,type,isGlobal)](#M-Exiled-API-Features-Badge-#ctor-System-String,System-String,System-Int32,System-Boolean- 'Exiled.API.Features.Badge.#ctor(System.String,System.String,System.Int32,System.Boolean)')
  - [Color](#P-Exiled-API-Features-Badge-Color 'Exiled.API.Features.Badge.Color')
  - [IsGlobal](#P-Exiled-API-Features-Badge-IsGlobal 'Exiled.API.Features.Badge.IsGlobal')
  - [Text](#P-Exiled-API-Features-Badge-Text 'Exiled.API.Features.Badge.Text')
  - [Type](#P-Exiled-API-Features-Badge-Type 'Exiled.API.Features.Badge.Type')
- [Cassie](#T-Exiled-API-Features-Cassie 'Exiled.API.Features.Cassie')
  - [MtfRespawn](#P-Exiled-API-Features-Cassie-MtfRespawn 'Exiled.API.Features.Cassie.MtfRespawn')
  - [DelayedMessage(message,delay,isHeld,isNoisy)](#M-Exiled-API-Features-Cassie-DelayedMessage-System-String,System-Single,System-Boolean,System-Boolean- 'Exiled.API.Features.Cassie.DelayedMessage(System.String,System.Single,System.Boolean,System.Boolean)')
  - [Message(message,isHeld,isNoisy)](#M-Exiled-API-Features-Cassie-Message-System-String,System-Boolean,System-Boolean- 'Exiled.API.Features.Cassie.Message(System.String,System.Boolean,System.Boolean)')
- [Config](#T-Exiled-API-Extensions-Config 'Exiled.API.Extensions.Config')
  - [GetStringDictionary(config,key,defaultValue)](#M-Exiled-API-Extensions-Config-GetStringDictionary-YamlConfig,System-String,System-Collections-Generic-Dictionary{System-String,System-String}- 'Exiled.API.Extensions.Config.GetStringDictionary(YamlConfig,System.String,System.Collections.Generic.Dictionary{System.String,System.String})')
  - [GetStringList(config,key,defaultValue)](#M-Exiled-API-Extensions-Config-GetStringList-YamlConfig,System-String,System-Collections-Generic-List{System-String}- 'Exiled.API.Extensions.Config.GetStringList(YamlConfig,System.String,System.Collections.Generic.List{System.String})')
- [EnvironmentType](#T-Exiled-API-Enums-EnvironmentType 'Exiled.API.Enums.EnvironmentType')
  - [Development](#F-Exiled-API-Enums-EnvironmentType-Development 'Exiled.API.Enums.EnvironmentType.Development')
  - [Production](#F-Exiled-API-Enums-EnvironmentType-Production 'Exiled.API.Enums.EnvironmentType.Production')
  - [Testing](#F-Exiled-API-Enums-EnvironmentType-Testing 'Exiled.API.Enums.EnvironmentType.Testing')
- [Event](#T-Exiled-API-Extensions-Event 'Exiled.API.Extensions.Event')
  - [HandleSafely(eventName,action,instance,args)](#M-Exiled-API-Extensions-Event-HandleSafely-System-String,System-Reflection-MethodInfo,System-Object,System-Object[]- 'Exiled.API.Extensions.Event.HandleSafely(System.String,System.Reflection.MethodInfo,System.Object,System.Object[])')
  - [InvokeSafely(ev,args)](#M-Exiled-API-Extensions-Event-InvokeSafely-System-MulticastDelegate,System-Object[]- 'Exiled.API.Extensions.Event.InvokeSafely(System.MulticastDelegate,System.Object[])')
- [IConfig](#T-Exiled-API-Interfaces-IConfig 'Exiled.API.Interfaces.IConfig')
  - [IsEnabled](#P-Exiled-API-Interfaces-IConfig-IsEnabled 'Exiled.API.Interfaces.IConfig.IsEnabled')
  - [Prefix](#P-Exiled-API-Interfaces-IConfig-Prefix 'Exiled.API.Interfaces.IConfig.Prefix')
  - [Reload()](#M-Exiled-API-Interfaces-IConfig-Reload 'Exiled.API.Interfaces.IConfig.Reload')
- [Item](#T-Exiled-API-Extensions-Item 'Exiled.API.Extensions.Item')
  - [GetWeaponAmmo(weapon)](#M-Exiled-API-Extensions-Item-GetWeaponAmmo-Inventory-SyncItemInfo- 'Exiled.API.Extensions.Item.GetWeaponAmmo(Inventory.SyncItemInfo)')
  - [IsAmmo(item)](#M-Exiled-API-Extensions-Item-IsAmmo-ItemType- 'Exiled.API.Extensions.Item.IsAmmo(ItemType)')
  - [IsKeycard(type)](#M-Exiled-API-Extensions-Item-IsKeycard-ItemType- 'Exiled.API.Extensions.Item.IsKeycard(ItemType)')
  - [IsMedical(type)](#M-Exiled-API-Extensions-Item-IsMedical-ItemType- 'Exiled.API.Extensions.Item.IsMedical(ItemType)')
  - [IsSCP(type)](#M-Exiled-API-Extensions-Item-IsSCP-ItemType- 'Exiled.API.Extensions.Item.IsSCP(ItemType)')
  - [IsThrowable(type)](#M-Exiled-API-Extensions-Item-IsThrowable-ItemType- 'Exiled.API.Extensions.Item.IsThrowable(ItemType)')
  - [IsUtility(type)](#M-Exiled-API-Extensions-Item-IsUtility-ItemType- 'Exiled.API.Extensions.Item.IsUtility(ItemType)')
  - [IsWeapon(type,checkMicro)](#M-Exiled-API-Extensions-Item-IsWeapon-ItemType,System-Boolean- 'Exiled.API.Extensions.Item.IsWeapon(ItemType,System.Boolean)')
  - [SetWeaponAmmo(list,weapon,amount)](#M-Exiled-API-Extensions-Item-SetWeaponAmmo-Inventory-SyncListItemInfo,Inventory-SyncItemInfo,System-Int32- 'Exiled.API.Extensions.Item.SetWeaponAmmo(Inventory.SyncListItemInfo,Inventory.SyncItemInfo,System.Int32)')
  - [SetWeaponAmmo(player,weapon,amount)](#M-Exiled-API-Extensions-Item-SetWeaponAmmo-Exiled-API-Features-Player,Inventory-SyncItemInfo,System-Int32- 'Exiled.API.Extensions.Item.SetWeaponAmmo(Exiled.API.Features.Player,Inventory.SyncItemInfo,System.Int32)')
  - [Spawn(itemType,durability,position,rotation,sight,barrel,other)](#M-Exiled-API-Extensions-Item-Spawn-ItemType,System-Single,UnityEngine-Vector3,UnityEngine-Quaternion,System-Int32,System-Int32,System-Int32- 'Exiled.API.Extensions.Item.Spawn(ItemType,System.Single,UnityEngine.Vector3,UnityEngine.Quaternion,System.Int32,System.Int32,System.Int32)')
- [Log](#T-Exiled-API-Features-Log 'Exiled.API.Features.Log')
  - [Debug(message,canBeSent)](#M-Exiled-API-Features-Log-Debug-System-String,System-Boolean- 'Exiled.API.Features.Log.Debug(System.String,System.Boolean)')
  - [Error(message)](#M-Exiled-API-Features-Log-Error-System-String- 'Exiled.API.Features.Log.Error(System.String)')
  - [Info(message)](#M-Exiled-API-Features-Log-Info-System-String- 'Exiled.API.Features.Log.Info(System.String)')
  - [Send(message,level,color)](#M-Exiled-API-Features-Log-Send-System-String,Discord-LogLevel,System-ConsoleColor- 'Exiled.API.Features.Log.Send(System.String,Discord.LogLevel,System.ConsoleColor)')
  - [Warn(message)](#M-Exiled-API-Features-Log-Warn-System-String- 'Exiled.API.Features.Log.Warn(System.String)')
- [LogLevel](#T-Exiled-API-Enums-LogLevel 'Exiled.API.Enums.LogLevel')
  - [Debug](#F-Exiled-API-Enums-LogLevel-Debug 'Exiled.API.Enums.LogLevel.Debug')
  - [Error](#F-Exiled-API-Enums-LogLevel-Error 'Exiled.API.Enums.LogLevel.Error')
  - [Info](#F-Exiled-API-Enums-LogLevel-Info 'Exiled.API.Enums.LogLevel.Info')
  - [Warn](#F-Exiled-API-Enums-LogLevel-Warn 'Exiled.API.Enums.LogLevel.Warn')
- [Map](#T-Exiled-API-Features-Map 'Exiled.API.Features.Map')
  - [ActivatedGenerators](#P-Exiled-API-Features-Map-ActivatedGenerators 'Exiled.API.Features.Map.ActivatedGenerators')
  - [Cameras](#P-Exiled-API-Features-Map-Cameras 'Exiled.API.Features.Map.Cameras')
  - [Doors](#P-Exiled-API-Features-Map-Doors 'Exiled.API.Features.Map.Doors')
  - [IsLCZDecontaminated](#P-Exiled-API-Features-Map-IsLCZDecontaminated 'Exiled.API.Features.Map.IsLCZDecontaminated')
  - [Lifts](#P-Exiled-API-Features-Map-Lifts 'Exiled.API.Features.Map.Lifts')
  - [Rooms](#P-Exiled-API-Features-Map-Rooms 'Exiled.API.Features.Map.Rooms')
  - [TeslaGates](#P-Exiled-API-Features-Map-TeslaGates 'Exiled.API.Features.Map.TeslaGates')
  - [Broadcast(duration,message,type)](#M-Exiled-API-Features-Map-Broadcast-System-UInt16,System-String,Broadcast-BroadcastFlags- 'Exiled.API.Features.Map.Broadcast(System.UInt16,System.String,Broadcast.BroadcastFlags)')
  - [ClearBroadcasts()](#M-Exiled-API-Features-Map-ClearBroadcasts 'Exiled.API.Features.Map.ClearBroadcasts')
  - [GetRandomSpawnPoint(roleType)](#M-Exiled-API-Features-Map-GetRandomSpawnPoint-RoleType- 'Exiled.API.Features.Map.GetRandomSpawnPoint(RoleType)')
  - [StartDecontamination()](#M-Exiled-API-Features-Map-StartDecontamination 'Exiled.API.Features.Map.StartDecontamination')
  - [TurnOffAllLights(duration,isHeavyContainmentZoneOnly)](#M-Exiled-API-Features-Map-TurnOffAllLights-System-Single,System-Boolean- 'Exiled.API.Features.Map.TurnOffAllLights(System.Single,System.Boolean)')
- [Paths](#T-Exiled-API-Features-Paths 'Exiled.API.Features.Paths')
  - [AppData](#P-Exiled-API-Features-Paths-AppData 'Exiled.API.Features.Paths.AppData')
  - [Config](#P-Exiled-API-Features-Paths-Config 'Exiled.API.Features.Paths.Config')
  - [Dependencies](#P-Exiled-API-Features-Paths-Dependencies 'Exiled.API.Features.Paths.Dependencies')
  - [Exiled](#P-Exiled-API-Features-Paths-Exiled 'Exiled.API.Features.Paths.Exiled')
  - [Log](#P-Exiled-API-Features-Paths-Log 'Exiled.API.Features.Paths.Log')
  - [ManagedAssemblies](#P-Exiled-API-Features-Paths-ManagedAssemblies 'Exiled.API.Features.Paths.ManagedAssemblies')
  - [Plugins](#P-Exiled-API-Features-Paths-Plugins 'Exiled.API.Features.Paths.Plugins')
- [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player')
  - [#ctor(referenceHub)](#M-Exiled-API-Features-Player-#ctor-ReferenceHub- 'Exiled.API.Features.Player.#ctor(ReferenceHub)')
  - [Abilities](#P-Exiled-API-Features-Player-Abilities 'Exiled.API.Features.Player.Abilities')
  - [AdrenalineHealth](#P-Exiled-API-Features-Player-AdrenalineHealth 'Exiled.API.Features.Player.AdrenalineHealth')
  - [AuthenticationType](#P-Exiled-API-Features-Player-AuthenticationType 'Exiled.API.Features.Player.AuthenticationType')
  - [Camera](#P-Exiled-API-Features-Player-Camera 'Exiled.API.Features.Player.Camera')
  - [Connection](#P-Exiled-API-Features-Player-Connection 'Exiled.API.Features.Player.Connection')
  - [CufferId](#P-Exiled-API-Features-Player-CufferId 'Exiled.API.Features.Player.CufferId')
  - [CurrentItem](#P-Exiled-API-Features-Player-CurrentItem 'Exiled.API.Features.Player.CurrentItem')
  - [CurrentRoom](#P-Exiled-API-Features-Player-CurrentRoom 'Exiled.API.Features.Player.CurrentRoom')
  - [CustomUserId](#P-Exiled-API-Features-Player-CustomUserId 'Exiled.API.Features.Player.CustomUserId')
  - [Dictionary](#P-Exiled-API-Features-Player-Dictionary 'Exiled.API.Features.Player.Dictionary')
  - [Energy](#P-Exiled-API-Features-Player-Energy 'Exiled.API.Features.Player.Energy')
  - [Experience](#P-Exiled-API-Features-Player-Experience 'Exiled.API.Features.Player.Experience')
  - [GameObject](#P-Exiled-API-Features-Player-GameObject 'Exiled.API.Features.Player.GameObject')
  - [GlobalBadge](#P-Exiled-API-Features-Player-GlobalBadge 'Exiled.API.Features.Player.GlobalBadge')
  - [Group](#P-Exiled-API-Features-Player-Group 'Exiled.API.Features.Player.Group')
  - [GroupName](#P-Exiled-API-Features-Player-GroupName 'Exiled.API.Features.Player.GroupName')
  - [Health](#P-Exiled-API-Features-Player-Health 'Exiled.API.Features.Player.Health')
  - [IPAddress](#P-Exiled-API-Features-Player-IPAddress 'Exiled.API.Features.Player.IPAddress')
  - [Id](#P-Exiled-API-Features-Player-Id 'Exiled.API.Features.Player.Id')
  - [IdsCache](#P-Exiled-API-Features-Player-IdsCache 'Exiled.API.Features.Player.IdsCache')
  - [Inventory](#P-Exiled-API-Features-Player-Inventory 'Exiled.API.Features.Player.Inventory')
  - [IsBypassModeEnabled](#P-Exiled-API-Features-Player-IsBypassModeEnabled 'Exiled.API.Features.Player.IsBypassModeEnabled')
  - [IsCuffed](#P-Exiled-API-Features-Player-IsCuffed 'Exiled.API.Features.Player.IsCuffed')
  - [IsDead](#P-Exiled-API-Features-Player-IsDead 'Exiled.API.Features.Player.IsDead')
  - [IsFriendlyFireEnabled](#P-Exiled-API-Features-Player-IsFriendlyFireEnabled 'Exiled.API.Features.Player.IsFriendlyFireEnabled')
  - [IsGodModeEnabled](#P-Exiled-API-Features-Player-IsGodModeEnabled 'Exiled.API.Features.Player.IsGodModeEnabled')
  - [IsHost](#P-Exiled-API-Features-Player-IsHost 'Exiled.API.Features.Player.IsHost')
  - [IsIntercomMuted](#P-Exiled-API-Features-Player-IsIntercomMuted 'Exiled.API.Features.Player.IsIntercomMuted')
  - [IsInvisible](#P-Exiled-API-Features-Player-IsInvisible 'Exiled.API.Features.Player.IsInvisible')
  - [IsMuted](#P-Exiled-API-Features-Player-IsMuted 'Exiled.API.Features.Player.IsMuted')
  - [IsNTF](#P-Exiled-API-Features-Player-IsNTF 'Exiled.API.Features.Player.IsNTF')
  - [IsOverwatchEnabled](#P-Exiled-API-Features-Player-IsOverwatchEnabled 'Exiled.API.Features.Player.IsOverwatchEnabled')
  - [IsReloading](#P-Exiled-API-Features-Player-IsReloading 'Exiled.API.Features.Player.IsReloading')
  - [IsStaffBypassEnabled](#P-Exiled-API-Features-Player-IsStaffBypassEnabled 'Exiled.API.Features.Player.IsStaffBypassEnabled')
  - [IsZooming](#P-Exiled-API-Features-Player-IsZooming 'Exiled.API.Features.Player.IsZooming')
  - [Level](#P-Exiled-API-Features-Player-Level 'Exiled.API.Features.Player.Level')
  - [Levels](#P-Exiled-API-Features-Player-Levels 'Exiled.API.Features.Player.Levels')
  - [List](#P-Exiled-API-Features-Player-List 'Exiled.API.Features.Player.List')
  - [LockedDoors](#P-Exiled-API-Features-Player-LockedDoors 'Exiled.API.Features.Player.LockedDoors')
  - [MaxAdrenalineHealth](#P-Exiled-API-Features-Player-MaxAdrenalineHealth 'Exiled.API.Features.Player.MaxAdrenalineHealth')
  - [MaxEnergy](#P-Exiled-API-Features-Player-MaxEnergy 'Exiled.API.Features.Player.MaxEnergy')
  - [MaxHealth](#P-Exiled-API-Features-Player-MaxHealth 'Exiled.API.Features.Player.MaxHealth')
  - [Nickname](#P-Exiled-API-Features-Player-Nickname 'Exiled.API.Features.Player.Nickname')
  - [PlayerCamera](#P-Exiled-API-Features-Player-PlayerCamera 'Exiled.API.Features.Player.PlayerCamera')
  - [Position](#P-Exiled-API-Features-Player-Position 'Exiled.API.Features.Player.Position')
  - [RankColor](#P-Exiled-API-Features-Player-RankColor 'Exiled.API.Features.Player.RankColor')
  - [RankName](#P-Exiled-API-Features-Player-RankName 'Exiled.API.Features.Player.RankName')
  - [ReferenceHub](#P-Exiled-API-Features-Player-ReferenceHub 'Exiled.API.Features.Player.ReferenceHub')
  - [Role](#P-Exiled-API-Features-Player-Role 'Exiled.API.Features.Player.Role')
  - [Rotation](#P-Exiled-API-Features-Player-Rotation 'Exiled.API.Features.Player.Rotation')
  - [Rotations](#P-Exiled-API-Features-Player-Rotations 'Exiled.API.Features.Player.Rotations')
  - [Scale](#P-Exiled-API-Features-Player-Scale 'Exiled.API.Features.Player.Scale')
  - [Side](#P-Exiled-API-Features-Player-Side 'Exiled.API.Features.Player.Side')
  - [Speaker](#P-Exiled-API-Features-Player-Speaker 'Exiled.API.Features.Player.Speaker')
  - [TargetGhosts](#P-Exiled-API-Features-Player-TargetGhosts 'Exiled.API.Features.Player.TargetGhosts')
  - [Team](#P-Exiled-API-Features-Player-Team 'Exiled.API.Features.Player.Team')
  - [UserId](#P-Exiled-API-Features-Player-UserId 'Exiled.API.Features.Player.UserId')
  - [UserIdsCache](#P-Exiled-API-Features-Player-UserIdsCache 'Exiled.API.Features.Player.UserIdsCache')
  - [AddItem(itemType)](#M-Exiled-API-Features-Player-AddItem-ItemType- 'Exiled.API.Features.Player.AddItem(ItemType)')
  - [AddItem(item)](#M-Exiled-API-Features-Player-AddItem-Inventory-SyncItemInfo- 'Exiled.API.Features.Player.AddItem(Inventory.SyncItemInfo)')
  - [Ban(duration,reason,issuer)](#M-Exiled-API-Features-Player-Ban-System-Int32,System-String,System-String- 'Exiled.API.Features.Player.Ban(System.Int32,System.String,System.String)')
  - [BlinkTag()](#M-Exiled-API-Features-Player-BlinkTag 'Exiled.API.Features.Player.BlinkTag')
  - [Broadcast(duration,message,type)](#M-Exiled-API-Features-Player-Broadcast-System-UInt16,System-String,Broadcast-BroadcastFlags- 'Exiled.API.Features.Player.Broadcast(System.UInt16,System.String,Broadcast.BroadcastFlags)')
  - [ClearBroadcasts()](#M-Exiled-API-Features-Player-ClearBroadcasts 'Exiled.API.Features.Player.ClearBroadcasts')
  - [ClearInventory()](#M-Exiled-API-Features-Player-ClearInventory 'Exiled.API.Features.Player.ClearInventory')
  - [Disconnect(reason)](#M-Exiled-API-Features-Player-Disconnect-System-String- 'Exiled.API.Features.Player.Disconnect(System.String)')
  - [DropItem(item)](#M-Exiled-API-Features-Player-DropItem-Inventory-SyncItemInfo- 'Exiled.API.Features.Player.DropItem(Inventory.SyncItemInfo)')
  - [Get(gameObject)](#M-Exiled-API-Features-Player-Get-UnityEngine-GameObject- 'Exiled.API.Features.Player.Get(UnityEngine.GameObject)')
  - [Get(id)](#M-Exiled-API-Features-Player-Get-System-Int32- 'Exiled.API.Features.Player.Get(System.Int32)')
  - [Get(args)](#M-Exiled-API-Features-Player-Get-System-String- 'Exiled.API.Features.Player.Get(System.String)')
  - [GetAmmo(ammoType)](#M-Exiled-API-Features-Player-GetAmmo-Exiled-API-Enums-AmmoType- 'Exiled.API.Features.Player.GetAmmo(Exiled.API.Enums.AmmoType)')
  - [GetCameraById(cameraId)](#M-Exiled-API-Features-Player-GetCameraById-System-UInt16- 'Exiled.API.Features.Player.GetCameraById(System.UInt16)')
  - [Handcuff(cuffer)](#M-Exiled-API-Features-Player-Handcuff-Exiled-API-Features-Player- 'Exiled.API.Features.Player.Handcuff(Exiled.API.Features.Player)')
  - [HideTag()](#M-Exiled-API-Features-Player-HideTag 'Exiled.API.Features.Player.HideTag')
  - [Kick(reason,issuer)](#M-Exiled-API-Features-Player-Kick-System-String,System-String- 'Exiled.API.Features.Player.Kick(System.String,System.String)')
  - [Kill(damageType)](#M-Exiled-API-Features-Player-Kill-DamageTypes-DamageType- 'Exiled.API.Features.Player.Kill(DamageTypes.DamageType)')
  - [RemoteAdminMessage(message,success,pluginName)](#M-Exiled-API-Features-Player-RemoteAdminMessage-System-String,System-Boolean,System-String- 'Exiled.API.Features.Player.RemoteAdminMessage(System.String,System.Boolean,System.String)')
  - [RemoveItem(item)](#M-Exiled-API-Features-Player-RemoveItem-Inventory-SyncItemInfo- 'Exiled.API.Features.Player.RemoveItem(Inventory.SyncItemInfo)')
  - [RemoveItem()](#M-Exiled-API-Features-Player-RemoveItem 'Exiled.API.Features.Player.RemoveItem')
  - [ResetInventory(newItems)](#M-Exiled-API-Features-Player-ResetInventory-System-Collections-Generic-List{Inventory-SyncItemInfo}- 'Exiled.API.Features.Player.ResetInventory(System.Collections.Generic.List{Inventory.SyncItemInfo})')
  - [SendConsoleMessage(message,color)](#M-Exiled-API-Features-Player-SendConsoleMessage-System-String,System-String- 'Exiled.API.Features.Player.SendConsoleMessage(System.String,System.String)')
  - [SendConsoleMessage(target,message,color)](#M-Exiled-API-Features-Player-SendConsoleMessage-Exiled-API-Features-Player,System-String,System-String- 'Exiled.API.Features.Player.SendConsoleMessage(Exiled.API.Features.Player,System.String,System.String)')
  - [SetAmmo(ammoType,amount)](#M-Exiled-API-Features-Player-SetAmmo-Exiled-API-Enums-AmmoType,System-UInt32- 'Exiled.API.Features.Player.SetAmmo(Exiled.API.Enums.AmmoType,System.UInt32)')
  - [SetCamera(id)](#M-Exiled-API-Features-Player-SetCamera-System-UInt16- 'Exiled.API.Features.Player.SetCamera(System.UInt16)')
  - [SetRank(name,group)](#M-Exiled-API-Features-Player-SetRank-System-String,UserGroup- 'Exiled.API.Features.Player.SetRank(System.String,UserGroup)')
  - [SetRole(newRole,lite,isEscaped)](#M-Exiled-API-Features-Player-SetRole-RoleType,System-Boolean,System-Boolean- 'Exiled.API.Features.Player.SetRole(RoleType,System.Boolean,System.Boolean)')
  - [ShowTag(isGlobal)](#M-Exiled-API-Features-Player-ShowTag-System-Boolean- 'Exiled.API.Features.Player.ShowTag(System.Boolean)')
- [Plugin](#T-Exiled-API-Features-Plugin 'Exiled.API.Features.Plugin')
  - [Config](#P-Exiled-API-Features-Plugin-Config 'Exiled.API.Features.Plugin.Config')
  - [Name](#P-Exiled-API-Features-Plugin-Name 'Exiled.API.Features.Plugin.Name')
  - [RequiredExiledVersion](#P-Exiled-API-Features-Plugin-RequiredExiledVersion 'Exiled.API.Features.Plugin.RequiredExiledVersion')
  - [Version](#P-Exiled-API-Features-Plugin-Version 'Exiled.API.Features.Plugin.Version')
  - [OnDisabled()](#M-Exiled-API-Features-Plugin-OnDisabled 'Exiled.API.Features.Plugin.OnDisabled')
  - [OnEnabled()](#M-Exiled-API-Features-Plugin-OnEnabled 'Exiled.API.Features.Plugin.OnEnabled')
  - [OnReloaded()](#M-Exiled-API-Features-Plugin-OnReloaded 'Exiled.API.Features.Plugin.OnReloaded')
- [Reflection](#T-Exiled-API-Extensions-Reflection 'Exiled.API.Extensions.Reflection')
  - [InvokeStaticMethod(type,methodName,param)](#M-Exiled-API-Extensions-Reflection-InvokeStaticMethod-System-Type,System-String,System-Object[]- 'Exiled.API.Extensions.Reflection.InvokeStaticMethod(System.Type,System.String,System.Object[])')
- [Role](#T-Exiled-API-Extensions-Role 'Exiled.API.Extensions.Role')
  - [GetTeam(roleType)](#M-Exiled-API-Extensions-Role-GetTeam-RoleType- 'Exiled.API.Extensions.Role.GetTeam(RoleType)')
- [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room')
  - [#ctor(name,transform,position)](#M-Exiled-API-Features-Room-#ctor-System-String,UnityEngine-Transform,UnityEngine-Vector3- 'Exiled.API.Features.Room.#ctor(System.String,UnityEngine.Transform,UnityEngine.Vector3)')
  - [Name](#P-Exiled-API-Features-Room-Name 'Exiled.API.Features.Room.Name')
  - [Players](#P-Exiled-API-Features-Room-Players 'Exiled.API.Features.Room.Players')
  - [Position](#P-Exiled-API-Features-Room-Position 'Exiled.API.Features.Room.Position')
  - [Transform](#P-Exiled-API-Features-Room-Transform 'Exiled.API.Features.Room.Transform')
  - [Zone](#P-Exiled-API-Features-Room-Zone 'Exiled.API.Features.Room.Zone')
- [Round](#T-Exiled-API-Features-Round 'Exiled.API.Features.Round')
  - [ElapsedTime](#P-Exiled-API-Features-Round-ElapsedTime 'Exiled.API.Features.Round.ElapsedTime')
  - [IsLobbyLocked](#P-Exiled-API-Features-Round-IsLobbyLocked 'Exiled.API.Features.Round.IsLobbyLocked')
  - [IsLocked](#P-Exiled-API-Features-Round-IsLocked 'Exiled.API.Features.Round.IsLocked')
  - [IsStarted](#P-Exiled-API-Features-Round-IsStarted 'Exiled.API.Features.Round.IsStarted')
  - [StartedTime](#P-Exiled-API-Features-Round-StartedTime 'Exiled.API.Features.Round.StartedTime')
- [Scp914](#T-Exiled-API-Features-Scp914 'Exiled.API.Features.Scp914')
  - [ConfigMode](#P-Exiled-API-Features-Scp914-ConfigMode 'Exiled.API.Features.Scp914.ConfigMode')
  - [IntakeBooth](#P-Exiled-API-Features-Scp914-IntakeBooth 'Exiled.API.Features.Scp914.IntakeBooth')
  - [IsWorking](#P-Exiled-API-Features-Scp914-IsWorking 'Exiled.API.Features.Scp914.IsWorking')
  - [KnobStatus](#P-Exiled-API-Features-Scp914-KnobStatus 'Exiled.API.Features.Scp914.KnobStatus')
  - [OutputBooth](#P-Exiled-API-Features-Scp914-OutputBooth 'Exiled.API.Features.Scp914.OutputBooth')
  - [Recipes](#P-Exiled-API-Features-Scp914-Recipes 'Exiled.API.Features.Scp914.Recipes')
  - [Start()](#M-Exiled-API-Features-Scp914-Start 'Exiled.API.Features.Scp914.Start')
- [Server](#T-Exiled-API-Features-Server 'Exiled.API.Features.Server')
  - [BanPlayer](#P-Exiled-API-Features-Server-BanPlayer 'Exiled.API.Features.Server.BanPlayer')
  - [Broadcast](#P-Exiled-API-Features-Server-Broadcast 'Exiled.API.Features.Server.Broadcast')
  - [FriendlyFire](#P-Exiled-API-Features-Server-FriendlyFire 'Exiled.API.Features.Server.FriendlyFire')
  - [Host](#P-Exiled-API-Features-Server-Host 'Exiled.API.Features.Server.Host')
  - [Name](#P-Exiled-API-Features-Server-Name 'Exiled.API.Features.Server.Name')
  - [Port](#P-Exiled-API-Features-Server-Port 'Exiled.API.Features.Server.Port')
  - [SendSpawnMessage](#P-Exiled-API-Features-Server-SendSpawnMessage 'Exiled.API.Features.Server.SendSpawnMessage')
- [Side](#T-Exiled-API-Enums-Side 'Exiled.API.Enums.Side')
  - [ChaosInsurgency](#F-Exiled-API-Enums-Side-ChaosInsurgency 'Exiled.API.Enums.Side.ChaosInsurgency')
  - [Mtf](#F-Exiled-API-Enums-Side-Mtf 'Exiled.API.Enums.Side.Mtf')
  - [None](#F-Exiled-API-Enums-Side-None 'Exiled.API.Enums.Side.None')
  - [Scp](#F-Exiled-API-Enums-Side-Scp 'Exiled.API.Enums.Side.Scp')
  - [Tutorial](#F-Exiled-API-Enums-Side-Tutorial 'Exiled.API.Enums.Side.Tutorial')
- [String](#T-Exiled-API-Extensions-String 'Exiled.API.Extensions.String')
  - [ExtractCommand(commandLine)](#M-Exiled-API-Extensions-String-ExtractCommand-System-String- 'Exiled.API.Extensions.String.ExtractCommand(System.String)')
  - [GetDistance(firstString,secondString)](#M-Exiled-API-Extensions-String-GetDistance-System-String,System-String- 'Exiled.API.Extensions.String.GetDistance(System.String,System.String)')
- [Warhead](#T-Exiled-API-Features-Warhead 'Exiled.API.Features.Warhead')
  - [Controller](#P-Exiled-API-Features-Warhead-Controller 'Exiled.API.Features.Warhead.Controller')
  - [DetonationTimer](#P-Exiled-API-Features-Warhead-DetonationTimer 'Exiled.API.Features.Warhead.DetonationTimer')
  - [IsDetonated](#P-Exiled-API-Features-Warhead-IsDetonated 'Exiled.API.Features.Warhead.IsDetonated')
  - [IsInProgress](#P-Exiled-API-Features-Warhead-IsInProgress 'Exiled.API.Features.Warhead.IsInProgress')
  - [IsWarheadLocked](#P-Exiled-API-Features-Warhead-IsWarheadLocked 'Exiled.API.Features.Warhead.IsWarheadLocked')
  - [LeverStatus](#P-Exiled-API-Features-Warhead-LeverStatus 'Exiled.API.Features.Warhead.LeverStatus')
  - [SitePanel](#P-Exiled-API-Features-Warhead-SitePanel 'Exiled.API.Features.Warhead.SitePanel')
  - [Detonate()](#M-Exiled-API-Features-Warhead-Detonate 'Exiled.API.Features.Warhead.Detonate')
  - [Start()](#M-Exiled-API-Features-Warhead-Start 'Exiled.API.Features.Warhead.Start')
  - [Stop()](#M-Exiled-API-Features-Warhead-Stop 'Exiled.API.Features.Warhead.Stop')
- [ZoneType](#T-Exiled-API-Enums-ZoneType 'Exiled.API.Enums.ZoneType')
  - [Entrance](#F-Exiled-API-Enums-ZoneType-Entrance 'Exiled.API.Enums.ZoneType.Entrance')
  - [HeavyContainment](#F-Exiled-API-Enums-ZoneType-HeavyContainment 'Exiled.API.Enums.ZoneType.HeavyContainment')
  - [LightContainment](#F-Exiled-API-Enums-ZoneType-LightContainment 'Exiled.API.Enums.ZoneType.LightContainment')
  - [Surface](#F-Exiled-API-Enums-ZoneType-Surface 'Exiled.API.Enums.ZoneType.Surface')
  - [Unspecified](#F-Exiled-API-Enums-ZoneType-Unspecified 'Exiled.API.Enums.ZoneType.Unspecified')

<a name='T-Exiled-API-Enums-AmmoType'></a>
## AmmoType `type`

##### Namespace

Exiled.API.Enums

##### Summary

Ammo types present in the game.

<a name='F-Exiled-API-Enums-AmmoType-Nato556'></a>
### Nato556 `constants`

##### Summary

5.56mm Ammunition.
Used by [GunE11SR](#F-ItemType-GunE11SR 'ItemType.GunE11SR').

<a name='F-Exiled-API-Enums-AmmoType-Nato762'></a>
### Nato762 `constants`

##### Summary

7.62mm mm Ammunition.
Used by [GunMP7](#F-ItemType-GunMP7 'ItemType.GunMP7') and [GunLogicer](#F-ItemType-GunLogicer 'ItemType.GunLogicer').

<a name='F-Exiled-API-Enums-AmmoType-Nato9'></a>
### Nato9 `constants`

##### Summary

9mm Ammunition.
Used by [GunCOM15](#F-ItemType-GunCOM15 'ItemType.GunCOM15'), [GunProject90](#F-ItemType-GunProject90 'ItemType.GunProject90') and [GunUSP](#F-ItemType-GunUSP 'ItemType.GunUSP').

<a name='T-Exiled-API-Enums-AuthenticationType'></a>
## AuthenticationType `type`

##### Namespace

Exiled.API.Enums

##### Summary

Players authentication types.

<a name='F-Exiled-API-Enums-AuthenticationType-Discord'></a>
### Discord `constants`

##### Summary

Indicates that the player has been authenticated through Discord.

<a name='F-Exiled-API-Enums-AuthenticationType-Northwood'></a>
### Northwood `constants`

##### Summary

Indicates that the player has been authenticated as a Northwood staffer.

<a name='F-Exiled-API-Enums-AuthenticationType-Patreon'></a>
### Patreon `constants`

##### Summary

Indicates that the player has been authenticated as a Patreon.

<a name='F-Exiled-API-Enums-AuthenticationType-Steam'></a>
### Steam `constants`

##### Summary

Indicates that the player has been authenticated through Steam.

<a name='F-Exiled-API-Enums-AuthenticationType-Unknown'></a>
### Unknown `constants`

##### Summary

Indicates that the player has been authenticated through an unknown provider.

<a name='T-Exiled-API-Features-Badge'></a>
## Badge `type`

##### Namespace

Exiled.API.Features

##### Summary

Represents the in-game badge.

<a name='M-Exiled-API-Features-Badge-#ctor-System-String,System-String,System-Int32,System-Boolean-'></a>
### #ctor(text,color,type,isGlobal) `constructor`

##### Summary

Initializes a new instance of the [Badge](#T-Exiled-API-Features-Badge 'Exiled.API.Features.Badge') class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| text | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The badge text. |
| color | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The badge color. |
| type | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The badge type. |
| isGlobal | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether the badge is global or not. |

<a name='P-Exiled-API-Features-Badge-Color'></a>
### Color `property`

##### Summary

Gets the badge color.

<a name='P-Exiled-API-Features-Badge-IsGlobal'></a>
### IsGlobal `property`

##### Summary

Gets a value indicating whether the badge is global or not.

<a name='P-Exiled-API-Features-Badge-Text'></a>
### Text `property`

##### Summary

Gets the badge text.

<a name='P-Exiled-API-Features-Badge-Type'></a>
### Type `property`

##### Summary

Gets the badge type.

<a name='T-Exiled-API-Features-Cassie'></a>
## Cassie `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to use in-game C.A.S.S.I.E more easily.

<a name='P-Exiled-API-Features-Cassie-MtfRespawn'></a>
### MtfRespawn `property`

##### Summary

Gets the cached [MTFRespawn](#T-MTFRespawn 'MTFRespawn') component.

<a name='M-Exiled-API-Features-Cassie-DelayedMessage-System-String,System-Single,System-Boolean,System-Boolean-'></a>
### DelayedMessage(message,delay,isHeld,isNoisy) `method`

##### Summary

Reproduce a C.A.S.S.I.E message after a certain amount of seconds.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be reproduced. |
| delay | [System.Single](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Single 'System.Single') | The seconds that have to pass, before reproducing the message. |
| isHeld | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether C.A.S.S.I.E has to hold the message. |
| isNoisy | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether C.A.S.S.I.E has to make noises or not during the message. |

<a name='M-Exiled-API-Features-Cassie-Message-System-String,System-Boolean,System-Boolean-'></a>
### Message(message,isHeld,isNoisy) `method`

##### Summary

Reproduce a C.A.S.S.I.E message.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be reproduced. |
| isHeld | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether C.A.S.S.I.E has to hold the message. |
| isNoisy | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether C.A.S.S.I.E has to make noises or not during the message. |

<a name='T-Exiled-API-Extensions-Config'></a>
## Config `type`

##### Namespace

Exiled.API.Extensions

##### Summary

A set of extensions for [YamlConfig](#T-YamlConfig 'YamlConfig').

<a name='M-Exiled-API-Extensions-Config-GetStringDictionary-YamlConfig,System-String,System-Collections-Generic-Dictionary{System-String,System-String}-'></a>
### GetStringDictionary(config,key,defaultValue) `method`

##### Summary

Extension of [GetStringDictionary](#M-YamlConfig-GetStringDictionary-System-String- 'YamlConfig.GetStringDictionary(System.String)').

##### Returns

Returns a [Dictionary\`2](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.Dictionary`2 'System.Collections.Generic.Dictionary`2') from the configs, or the default value if empty.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| config | [YamlConfig](#T-YamlConfig 'YamlConfig') | The config instance. |
| key | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The config key. |
| defaultValue | [System.Collections.Generic.Dictionary{System.String,System.String}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.Dictionary 'System.Collections.Generic.Dictionary{System.String,System.String}') | The config default value. |

<a name='M-Exiled-API-Extensions-Config-GetStringList-YamlConfig,System-String,System-Collections-Generic-List{System-String}-'></a>
### GetStringList(config,key,defaultValue) `method`

##### Summary

Extension of [GetStringList](#M-YamlConfig-GetStringList-System-String- 'YamlConfig.GetStringList(System.String)').

##### Returns

Returns a [List\`1](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List`1 'System.Collections.Generic.List`1') from the configs, or the default value if empty.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| config | [YamlConfig](#T-YamlConfig 'YamlConfig') | The config instance. |
| key | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The config key. |
| defaultValue | [System.Collections.Generic.List{System.String}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List 'System.Collections.Generic.List{System.String}') | The config default value. |

<a name='T-Exiled-API-Enums-EnvironmentType'></a>
## EnvironmentType `type`

##### Namespace

Exiled.API.Enums

##### Summary

A set of environment types.

<a name='F-Exiled-API-Enums-EnvironmentType-Development'></a>
### Development `constants`

##### Summary

The development environment, for developers.

<a name='F-Exiled-API-Enums-EnvironmentType-Production'></a>
### Production `constants`

##### Summary

The production environment, for the public.

<a name='F-Exiled-API-Enums-EnvironmentType-Testing'></a>
### Testing `constants`

##### Summary

The testing environment, for testing things.

<a name='T-Exiled-API-Extensions-Event'></a>
## Event `type`

##### Namespace

Exiled.API.Extensions

##### Summary

A set of tools to execute events safely and without breaking other plugins.

<a name='M-Exiled-API-Extensions-Event-HandleSafely-System-String,System-Reflection-MethodInfo,System-Object,System-Object[]-'></a>
### HandleSafely(eventName,action,instance,args) `method`

##### Summary

Executes a [MethodInfo](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Reflection.MethodInfo 'System.Reflection.MethodInfo') safely.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| eventName | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The name of the event. |
| action | [System.Reflection.MethodInfo](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Reflection.MethodInfo 'System.Reflection.MethodInfo') | The method to invoke. |
| instance | [System.Object](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Object 'System.Object') | The instance that invoked the method. |
| args | [System.Object[]](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Object[] 'System.Object[]') | The method arguments. |

<a name='M-Exiled-API-Extensions-Event-InvokeSafely-System-MulticastDelegate,System-Object[]-'></a>
### InvokeSafely(ev,args) `method`

##### Summary

Executes all [MulticastDelegate](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.MulticastDelegate 'System.MulticastDelegate') listeners safely.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| ev | [System.MulticastDelegate](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.MulticastDelegate 'System.MulticastDelegate') | Delegates to be invoked. |
| args | [System.Object[]](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Object[] 'System.Object[]') | Delegates arguments. |

<a name='T-Exiled-API-Interfaces-IConfig'></a>
## IConfig `type`

##### Namespace

Exiled.API.Interfaces

##### Summary

Define the contract for basic config features.

<a name='P-Exiled-API-Interfaces-IConfig-IsEnabled'></a>
### IsEnabled `property`

##### Summary

Gets or sets a value indicating whether the plugin is enabled or not.

<a name='P-Exiled-API-Interfaces-IConfig-Prefix'></a>
### Prefix `property`

##### Summary

Gets the plugin config prefix.

<a name='M-Exiled-API-Interfaces-IConfig-Reload'></a>
### Reload() `method`

##### Summary

Reload the configs.

##### Parameters

This method has no parameters.

<a name='T-Exiled-API-Extensions-Item'></a>
## Item `type`

##### Namespace

Exiled.API.Extensions

##### Summary

A set of extensions for [ItemType](#T-ItemType 'ItemType').

<a name='M-Exiled-API-Extensions-Item-GetWeaponAmmo-Inventory-SyncItemInfo-'></a>
### GetWeaponAmmo(weapon) `method`

##### Summary

Get the ammo of an [SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo').

##### Returns

Returns the weapon left ammo.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| weapon | [Inventory.SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo') | The weapon to be get. |

<a name='M-Exiled-API-Extensions-Item-IsAmmo-ItemType-'></a>
### IsAmmo(item) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is an ammo.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is an ammo or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| item | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |

<a name='M-Exiled-API-Extensions-Item-IsKeycard-ItemType-'></a>
### IsKeycard(type) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is a keycard.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is a keycard or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |

<a name='M-Exiled-API-Extensions-Item-IsMedical-ItemType-'></a>
### IsMedical(type) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is a medical item.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is a medical item or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |

<a name='M-Exiled-API-Extensions-Item-IsSCP-ItemType-'></a>
### IsSCP(type) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is an SCP.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is an SCP or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |

<a name='M-Exiled-API-Extensions-Item-IsThrowable-ItemType-'></a>
### IsThrowable(type) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is a throwable item.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is a throwable item or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |

<a name='M-Exiled-API-Extensions-Item-IsUtility-ItemType-'></a>
### IsUtility(type) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is a utility item.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is an utilty item or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |

<a name='M-Exiled-API-Extensions-Item-IsWeapon-ItemType,System-Boolean-'></a>
### IsWeapon(type,checkMicro) `method`

##### Summary

Check if an [ItemType](#T-ItemType 'ItemType') is a weapon.

##### Returns

Returns whether the [ItemType](#T-ItemType 'ItemType') is a weapon or not.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [ItemType](#T-ItemType 'ItemType') | The item to be checked. |
| checkMicro | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether the MicroHID item should be taken into account or not. |

<a name='M-Exiled-API-Extensions-Item-SetWeaponAmmo-Inventory-SyncListItemInfo,Inventory-SyncItemInfo,System-Int32-'></a>
### SetWeaponAmmo(list,weapon,amount) `method`

##### Summary

Set the ammo of an [SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| list | [Inventory.SyncListItemInfo](#T-Inventory-SyncListItemInfo 'Inventory.SyncListItemInfo') | The list of items. |
| weapon | [Inventory.SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo') | The weapon to be changed. |
| amount | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The ammo amount. |

<a name='M-Exiled-API-Extensions-Item-SetWeaponAmmo-Exiled-API-Features-Player,Inventory-SyncItemInfo,System-Int32-'></a>
### SetWeaponAmmo(player,weapon,amount) `method`

##### Summary

Set the ammo value of an [SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| player | [Exiled.API.Features.Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') | The player instance. |
| weapon | [Inventory.SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo') | The weapon to be changed. |
| amount | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The ammo amount. |

<a name='M-Exiled-API-Extensions-Item-Spawn-ItemType,System-Single,UnityEngine-Vector3,UnityEngine-Quaternion,System-Int32,System-Int32,System-Int32-'></a>
### Spawn(itemType,durability,position,rotation,sight,barrel,other) `method`

##### Summary

Spawns an [ItemType](#T-ItemType 'ItemType') in a desired [Vector3](#T-UnityEngine-Vector3 'UnityEngine.Vector3') position.

##### Returns

Returns the spawned [Pickup](#T-Pickup 'Pickup').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| itemType | [ItemType](#T-ItemType 'ItemType') | The type of the item to be spawned. |
| durability | [System.Single](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Single 'System.Single') | The durability (or ammo, depends on the weapon) of the item. |
| position | [UnityEngine.Vector3](#T-UnityEngine-Vector3 'UnityEngine.Vector3') | Where the item will be spawned. |
| rotation | [UnityEngine.Quaternion](#T-UnityEngine-Quaternion 'UnityEngine.Quaternion') | The rotation. We recommend you to use [Euler](#M-UnityEngine-Quaternion-Euler-System-Single,System-Single,System-Single- 'UnityEngine.Quaternion.Euler(System.Single,System.Single,System.Single)'). |
| sight | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The sight the weapon will have (0 is nothing, 1 is the first sight available in the weapon manager, and so on). |
| barrel | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The barrel of the weapon (0 is no custom barrel, 1 is the first barrel available, and so on). |
| other | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | Other attachments like flashlight, laser or ammo counter. |

<a name='T-Exiled-API-Features-Log'></a>
## Log `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to print messages on the server console.

<a name='M-Exiled-API-Features-Log-Debug-System-String,System-Boolean-'></a>
### Debug(message,canBeSent) `method`

##### Summary

Sends a [Debug](#F-Discord-LogLevel-Debug 'Discord.LogLevel.Debug') level messages to the game console.
Server must have exiled_debug config enabled.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |
| canBeSent | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether the log can be sent or not. |

<a name='M-Exiled-API-Features-Log-Error-System-String-'></a>
### Error(message) `method`

##### Summary

Sends a [Error](#F-Discord-LogLevel-Error 'Discord.LogLevel.Error') level messages to the game console.
This should be used to send errors only.
It's recommended to send any messages in the catch block of a try/catch as errors with the exception string.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |

<a name='M-Exiled-API-Features-Log-Info-System-String-'></a>
### Info(message) `method`

##### Summary

Sends a [Info](#F-Discord-LogLevel-Info 'Discord.LogLevel.Info') level messages to the game console.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |

<a name='M-Exiled-API-Features-Log-Send-System-String,Discord-LogLevel,System-ConsoleColor-'></a>
### Send(message,level,color) `method`

##### Summary

Sends a log message to the game console.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |
| level | [Discord.LogLevel](#T-Discord-LogLevel 'Discord.LogLevel') | The message level of importance. |
| color | [System.ConsoleColor](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ConsoleColor 'System.ConsoleColor') | The message color. |

<a name='M-Exiled-API-Features-Log-Warn-System-String-'></a>
### Warn(message) `method`

##### Summary

Sends a [Warn](#F-Discord-LogLevel-Warn 'Discord.LogLevel.Warn') level messages to the game console.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |

<a name='T-Exiled-API-Enums-LogLevel'></a>
## LogLevel `type`

##### Namespace

Exiled.API.Enums

##### Summary

Importance levels of log messages.

<a name='F-Exiled-API-Enums-LogLevel-Debug'></a>
### Debug `constants`

##### Summary

Print a green debug on the game console.

<a name='F-Exiled-API-Enums-LogLevel-Error'></a>
### Error `constants`

##### Summary

Print a red error on the game console.

<a name='F-Exiled-API-Enums-LogLevel-Info'></a>
### Info `constants`

##### Summary

Print a grey information on the game console.

<a name='F-Exiled-API-Enums-LogLevel-Warn'></a>
### Warn `constants`

##### Summary

Print a yellow warning on the game console.

<a name='T-Exiled-API-Features-Map'></a>
## Map `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to handle the in-game map more easily.

<a name='P-Exiled-API-Features-Map-ActivatedGenerators'></a>
### ActivatedGenerators `property`

##### Summary

Gets the number of activated generators.

<a name='P-Exiled-API-Features-Map-Cameras'></a>
### Cameras `property`

##### Summary

Gets all cameras of SCP-079.

<a name='P-Exiled-API-Features-Map-Doors'></a>
### Doors `property`

##### Summary

Gets all [Door](#T-Door 'Door').

<a name='P-Exiled-API-Features-Map-IsLCZDecontaminated'></a>
### IsLCZDecontaminated `property`

##### Summary

Gets a value indicating whether the decontamination has been completed or not.

<a name='P-Exiled-API-Features-Map-Lifts'></a>
### Lifts `property`

##### Summary

Gets all [Lift](#T-Lift 'Lift').

<a name='P-Exiled-API-Features-Map-Rooms'></a>
### Rooms `property`

##### Summary

Gets all [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room').

<a name='P-Exiled-API-Features-Map-TeslaGates'></a>
### TeslaGates `property`

##### Summary

Gets all [TeslaGate](#T-TeslaGate 'TeslaGate').

<a name='M-Exiled-API-Features-Map-Broadcast-System-UInt16,System-String,Broadcast-BroadcastFlags-'></a>
### Broadcast(duration,message,type) `method`

##### Summary

Broadcasts a message to all players.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| duration | [System.UInt16](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.UInt16 'System.UInt16') | The duration in seconds. |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message that will be broadcast (supports Unity Rich Text formatting). |
| type | [Broadcast.BroadcastFlags](#T-Broadcast-BroadcastFlags 'Broadcast.BroadcastFlags') | The broadcast type. |

<a name='M-Exiled-API-Features-Map-ClearBroadcasts'></a>
### ClearBroadcasts() `method`

##### Summary

Clears all players' broadcasts.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Map-GetRandomSpawnPoint-RoleType-'></a>
### GetRandomSpawnPoint(roleType) `method`

##### Summary

Gets a random spawn point of a [RoleType](#T-RoleType 'RoleType').

##### Returns

Returns the spawn point [Vector3](#T-UnityEngine-Vector3 'UnityEngine.Vector3').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| roleType | [RoleType](#T-RoleType 'RoleType') | The [RoleType](#T-RoleType 'RoleType') to get the spawn point from. |

<a name='M-Exiled-API-Features-Map-StartDecontamination'></a>
### StartDecontamination() `method`

##### Summary

Starts the Decontamination process.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Map-TurnOffAllLights-System-Single,System-Boolean-'></a>
### TurnOffAllLights(duration,isHeavyContainmentZoneOnly) `method`

##### Summary

Turns off all lights of the facility (except for the entrance zone).

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| duration | [System.Single](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Single 'System.Single') | The duration of the blackout. |
| isHeavyContainmentZoneOnly | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether only the heavy containment zone lights have to be turned off or not. |

<a name='T-Exiled-API-Features-Paths'></a>
## Paths `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of useful paths.

<a name='P-Exiled-API-Features-Paths-AppData'></a>
### AppData `property`

##### Summary

Gets AppData path.

<a name='P-Exiled-API-Features-Paths-Config'></a>
### Config `property`

##### Summary

Gets or sets configs path.

<a name='P-Exiled-API-Features-Paths-Dependencies'></a>
### Dependencies `property`

##### Summary

Gets or sets Dependencies directory path.

<a name='P-Exiled-API-Features-Paths-Exiled'></a>
### Exiled `property`

##### Summary

Gets or sets exiled directory path.

<a name='P-Exiled-API-Features-Paths-Log'></a>
### Log `property`

##### Summary

Gets or sets logs path.

<a name='P-Exiled-API-Features-Paths-ManagedAssemblies'></a>
### ManagedAssemblies `property`

##### Summary

Gets managed assemblies directory path.

<a name='P-Exiled-API-Features-Paths-Plugins'></a>
### Plugins `property`

##### Summary

Gets or sets plugins path.

<a name='T-Exiled-API-Features-Player'></a>
## Player `type`

##### Namespace

Exiled.API.Features

##### Summary

Represents the in-game player, by encapsulating a [ReferenceHub](#T-ReferenceHub 'ReferenceHub').

<a name='M-Exiled-API-Features-Player-#ctor-ReferenceHub-'></a>
### #ctor(referenceHub) `constructor`

##### Summary

Initializes a new instance of the [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| referenceHub | [ReferenceHub](#T-ReferenceHub 'ReferenceHub') | The [ReferenceHub](#P-Exiled-API-Features-Player-ReferenceHub 'Exiled.API.Features.Player.ReferenceHub') of the player to be encapsulated. |

<a name='P-Exiled-API-Features-Player-Abilities'></a>
### Abilities `property`

##### Summary

Gets or sets the abilities of SCP-079. Can be null.

<a name='P-Exiled-API-Features-Player-AdrenalineHealth'></a>
### AdrenalineHealth `property`

##### Summary

Gets or sets the player's adrenaline health.

<a name='P-Exiled-API-Features-Player-AuthenticationType'></a>
### AuthenticationType `property`

##### Summary

*Inherit from parent.*

<a name='P-Exiled-API-Features-Player-Camera'></a>
### Camera `property`

##### Summary

Gets or sets the camera of SCP-079.

<a name='P-Exiled-API-Features-Player-Connection'></a>
### Connection `property`

##### Summary

Gets player's [NetworkConnection](#T-Mirror-NetworkConnection 'Mirror.NetworkConnection').

<a name='P-Exiled-API-Features-Player-CufferId'></a>
### CufferId `property`

##### Summary

Gets or sets a value indicating the cuffer [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') id.

<a name='P-Exiled-API-Features-Player-CurrentItem'></a>
### CurrentItem `property`

##### Summary

Gets or sets the item in the player's hand, returns the default value if empty.

<a name='P-Exiled-API-Features-Player-CurrentRoom'></a>
### CurrentRoom `property`

##### Summary

Gets the current room the player is in.

<a name='P-Exiled-API-Features-Player-CustomUserId'></a>
### CustomUserId `property`

##### Summary

Gets or sets the player's custom user id.

<a name='P-Exiled-API-Features-Player-Dictionary'></a>
### Dictionary `property`

##### Summary

Gets a [Dictionary\`2](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.Dictionary`2 'System.Collections.Generic.Dictionary`2') containing all [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') on the server.

<a name='P-Exiled-API-Features-Player-Energy'></a>
### Energy `property`

##### Summary

Gets or sets the energy of SCP-079.

<a name='P-Exiled-API-Features-Player-Experience'></a>
### Experience `property`

##### Summary

Gets or sets the experience of SCP-079.

<a name='P-Exiled-API-Features-Player-GameObject'></a>
### GameObject `property`

##### Summary

Gets the encapsulated [GameObject](#T-UnityEngine-GameObject 'UnityEngine.GameObject').

<a name='P-Exiled-API-Features-Player-GlobalBadge'></a>
### GlobalBadge `property`

##### Summary

Gets the global badge of the player, can be null if none.

<a name='P-Exiled-API-Features-Player-Group'></a>
### Group `property`

##### Summary

Gets or sets the player's group.

<a name='P-Exiled-API-Features-Player-GroupName'></a>
### GroupName `property`

##### Summary

Gets or sets the player's group name.

<a name='P-Exiled-API-Features-Player-Health'></a>
### Health `property`

##### Summary

Gets or sets the player's health.

<a name='P-Exiled-API-Features-Player-IPAddress'></a>
### IPAddress `property`

##### Summary

Gets or sets the player's IP address.

<a name='P-Exiled-API-Features-Player-Id'></a>
### Id `property`

##### Summary

Gets or sets the player's id.

<a name='P-Exiled-API-Features-Player-IdsCache'></a>
### IdsCache `property`

##### Summary

Gets a [Dictionary\`2](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.Dictionary`2 'System.Collections.Generic.Dictionary`2') containing cached [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') and their ids.

<a name='P-Exiled-API-Features-Player-Inventory'></a>
### Inventory `property`

##### Summary

Gets the player's inventory.

<a name='P-Exiled-API-Features-Player-IsBypassModeEnabled'></a>
### IsBypassModeEnabled `property`

##### Summary

Gets or sets a value indicating whether the player's bypass mode is enabled or not.

<a name='P-Exiled-API-Features-Player-IsCuffed'></a>
### IsCuffed `property`

##### Summary

Gets a value indicating whether the player is cuffed or not.

<a name='P-Exiled-API-Features-Player-IsDead'></a>
### IsDead `property`

##### Summary

Gets a value indicating whether the player is dead or not.

<a name='P-Exiled-API-Features-Player-IsFriendlyFireEnabled'></a>
### IsFriendlyFireEnabled `property`

##### Summary

Gets or sets a value indicating whether the player friendly fire is enabled or not.
This only isAllowed to deal friendly fire damage, not take friendly fire damage.

<a name='P-Exiled-API-Features-Player-IsGodModeEnabled'></a>
### IsGodModeEnabled `property`

##### Summary

Gets or sets a value indicating whether the player's godmode is enabled or not.

<a name='P-Exiled-API-Features-Player-IsHost'></a>
### IsHost `property`

##### Summary

Gets a value indicating whether the player is the host or not.

<a name='P-Exiled-API-Features-Player-IsIntercomMuted'></a>
### IsIntercomMuted `property`

##### Summary

Gets or sets a value indicating whether the player is intercom muted or not.

<a name='P-Exiled-API-Features-Player-IsInvisible'></a>
### IsInvisible `property`

##### Summary

Gets or sets a value indicating whether the player is invisible or not.

<a name='P-Exiled-API-Features-Player-IsMuted'></a>
### IsMuted `property`

##### Summary

Gets or sets a value indicating whether the player is muted or not.

<a name='P-Exiled-API-Features-Player-IsNTF'></a>
### IsNTF `property`

##### Summary

Gets a value indicating whether the player's role type is any NTF type [ReferenceHub](#P-Exiled-API-Features-Player-ReferenceHub 'Exiled.API.Features.Player.ReferenceHub').

<a name='P-Exiled-API-Features-Player-IsOverwatchEnabled'></a>
### IsOverwatchEnabled `property`

##### Summary

Gets or sets a value indicating whether the player's overwatch is enabled or not.

<a name='P-Exiled-API-Features-Player-IsReloading'></a>
### IsReloading `property`

##### Summary

Gets a value indicating whether the player is reloading or not.

<a name='P-Exiled-API-Features-Player-IsStaffBypassEnabled'></a>
### IsStaffBypassEnabled `property`

##### Summary

Gets a value indicating whether the staff bypass is enabled or not.

<a name='P-Exiled-API-Features-Player-IsZooming'></a>
### IsZooming `property`

##### Summary

Gets a value indicating whether the player is zooming or not.

<a name='P-Exiled-API-Features-Player-Level'></a>
### Level `property`

##### Summary

Gets or sets the level of SCP-079.

<a name='P-Exiled-API-Features-Player-Levels'></a>
### Levels `property`

##### Summary

Gets or sets the levels of SCP-079. Can be null.

<a name='P-Exiled-API-Features-Player-List'></a>
### List `property`

##### Summary

Gets a list of all [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player')'s on the server.

<a name='P-Exiled-API-Features-Player-LockedDoors'></a>
### LockedDoors `property`

##### Summary

Gets or sets the SCP-079 locked doors [SyncListString](#T-Mirror-SyncListString 'Mirror.SyncListString'). Can be null.

<a name='P-Exiled-API-Features-Player-MaxAdrenalineHealth'></a>
### MaxAdrenalineHealth `property`

##### Summary

Gets or sets the player's maximum adrenaline health.

<a name='P-Exiled-API-Features-Player-MaxEnergy'></a>
### MaxEnergy `property`

##### Summary

Gets or sets the SCP-079 max energy.

<a name='P-Exiled-API-Features-Player-MaxHealth'></a>
### MaxHealth `property`

##### Summary

Gets or sets the player's maximum health.

<a name='P-Exiled-API-Features-Player-Nickname'></a>
### Nickname `property`

##### Summary

Gets or sets the player's nickname.

<a name='P-Exiled-API-Features-Player-PlayerCamera'></a>
### PlayerCamera `property`

##### Summary

Gets the encapsulated [ReferenceHub](#P-Exiled-API-Features-Player-ReferenceHub 'Exiled.API.Features.Player.ReferenceHub')'s PlayerCamera.

<a name='P-Exiled-API-Features-Player-Position'></a>
### Position `property`

##### Summary

Gets or sets the player's position.

<a name='P-Exiled-API-Features-Player-RankColor'></a>
### RankColor `property`

##### Summary

Gets or sets the player's rank color.

<a name='P-Exiled-API-Features-Player-RankName'></a>
### RankName `property`

##### Summary

Gets or sets the player's rank name.

<a name='P-Exiled-API-Features-Player-ReferenceHub'></a>
### ReferenceHub `property`

##### Summary

Gets the encapsulated [ReferenceHub](#T-ReferenceHub 'ReferenceHub').

<a name='P-Exiled-API-Features-Player-Role'></a>
### Role `property`

##### Summary

Gets or sets the player's [RoleType](#T-RoleType 'RoleType').

<a name='P-Exiled-API-Features-Player-Rotation'></a>
### Rotation `property`

##### Summary

Gets or sets the player's rotation.

##### Returns

Returns the direction he's looking at, useful for Raycasts.

<a name='P-Exiled-API-Features-Player-Rotations'></a>
### Rotations `property`

##### Summary

Gets or sets the player's rotations.

##### Returns

Returns a [Vector2](#T-UnityEngine-Vector2 'UnityEngine.Vector2'), representing the directions he's looking at.

<a name='P-Exiled-API-Features-Player-Scale'></a>
### Scale `property`

##### Summary

Gets or sets the player's scale.

<a name='P-Exiled-API-Features-Player-Side'></a>
### Side `property`

##### Summary

Gets the player's [Side](#T-Exiled-API-Enums-Side 'Exiled.API.Enums.Side') they're currently in.

<a name='P-Exiled-API-Features-Player-Speaker'></a>
### Speaker `property`

##### Summary

Gets or sets the speaker of SCP-079. Can be null.

<a name='P-Exiled-API-Features-Player-TargetGhosts'></a>
### TargetGhosts `property`

##### Summary

Gets a list of player ids who can't see the player.

<a name='P-Exiled-API-Features-Player-Team'></a>
### Team `property`

##### Summary

Gets the player's [Team](#P-Exiled-API-Features-Player-Team 'Exiled.API.Features.Player.Team').

<a name='P-Exiled-API-Features-Player-UserId'></a>
### UserId `property`

##### Summary

Gets or sets the player's user id.

<a name='P-Exiled-API-Features-Player-UserIdsCache'></a>
### UserIdsCache `property`

##### Summary

Gets a [Dictionary\`2](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.Dictionary`2 'System.Collections.Generic.Dictionary`2') containing cached [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') and their user ids.

<a name='M-Exiled-API-Features-Player-AddItem-ItemType-'></a>
### AddItem(itemType) `method`

##### Summary

Add an item of the specified type with default durability(ammo/charge) and no mods to the player's inventory.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| itemType | [ItemType](#T-ItemType 'ItemType') | The item to be added. |

<a name='M-Exiled-API-Features-Player-AddItem-Inventory-SyncItemInfo-'></a>
### AddItem(item) `method`

##### Summary

Add an item with the specified info to a player's inventory.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| item | [Inventory.SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo') | The item to be added. |

<a name='M-Exiled-API-Features-Player-Ban-System-Int32,System-String,System-String-'></a>
### Ban(duration,reason,issuer) `method`

##### Summary

Bans a the player.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| duration | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The ban duration. |
| reason | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The ban reason. |
| issuer | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The ban issuer nickname. |

<a name='M-Exiled-API-Features-Player-BlinkTag'></a>
### BlinkTag() `method`

##### Summary

Blink the player's tag.

##### Returns

Used to wait.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Player-Broadcast-System-UInt16,System-String,Broadcast-BroadcastFlags-'></a>
### Broadcast(duration,message,type) `method`

##### Summary

A simple broadcast to a [ReferenceHub](#P-Exiled-API-Features-Player-ReferenceHub 'Exiled.API.Features.Player.ReferenceHub'). Doesn't get logged to the console and can be monospaced.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| duration | [System.UInt16](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.UInt16 'System.UInt16') | The broadcast duration. |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be broadcasted. |
| type | [Broadcast.BroadcastFlags](#T-Broadcast-BroadcastFlags 'Broadcast.BroadcastFlags') | The broadcast type. |

<a name='M-Exiled-API-Features-Player-ClearBroadcasts'></a>
### ClearBroadcasts() `method`

##### Summary

Clears the player's brodcast. Doesn't get logged to the console.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Player-ClearInventory'></a>
### ClearInventory() `method`

##### Summary

Clears the player's inventory.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Player-Disconnect-System-String-'></a>
### Disconnect(reason) `method`

##### Summary

Disconnects a [ReferenceHub](#P-Exiled-API-Features-Player-ReferenceHub 'Exiled.API.Features.Player.ReferenceHub').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| reason | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The disconnection reason. |

<a name='M-Exiled-API-Features-Player-DropItem-Inventory-SyncItemInfo-'></a>
### DropItem(item) `method`

##### Summary

Drops an item from the player's inventory.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| item | [Inventory.SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo') | The item to be dropped. |

<a name='M-Exiled-API-Features-Player-Get-UnityEngine-GameObject-'></a>
### Get(gameObject) `method`

##### Summary

Gets the Player belonging to the GameObject, if any.

##### Returns

Returns a player or null if not found.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| gameObject | [UnityEngine.GameObject](#T-UnityEngine-GameObject 'UnityEngine.GameObject') | The [GameObject](#T-UnityEngine-GameObject 'UnityEngine.GameObject'). |

<a name='M-Exiled-API-Features-Player-Get-System-Int32-'></a>
### Get(id) `method`

##### Summary

Gets the player belonging to the player with the specified id.

##### Returns

Returns the player found or null if not found.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | [System.Int32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Int32 'System.Int32') | The player id. |

<a name='M-Exiled-API-Features-Player-Get-System-String-'></a>
### Get(args) `method`

##### Summary

Gets the player by his identifier.

##### Returns

Returns the player found or null if not found.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| args | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The player's nickname, steamID64 or Discord ID. |

<a name='M-Exiled-API-Features-Player-GetAmmo-Exiled-API-Enums-AmmoType-'></a>
### GetAmmo(ammoType) `method`

##### Summary

Gets the amount of a specified [AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType').

##### Returns

Returns the amount of the chosen [AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| ammoType | [Exiled.API.Enums.AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType') | The [AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType') to get the amount from. |

<a name='M-Exiled-API-Features-Player-GetCameraById-System-UInt16-'></a>
### GetCameraById(cameraId) `method`

##### Summary

Gets the camera with the given ID.

##### Returns

[Camera079](#T-Camera079 'Camera079').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| cameraId | [System.UInt16](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.UInt16 'System.UInt16') | The camera id to be searched for. |

<a name='M-Exiled-API-Features-Player-Handcuff-Exiled-API-Features-Player-'></a>
### Handcuff(cuffer) `method`

##### Summary

Handcuff the player.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| cuffer | [Exiled.API.Features.Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') | The cuffer player. |

<a name='M-Exiled-API-Features-Player-HideTag'></a>
### HideTag() `method`

##### Summary

Hides the player's tag.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Player-Kick-System-String,System-String-'></a>
### Kick(reason,issuer) `method`

##### Summary

Kicks the player.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| reason | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The kick reason. |
| issuer | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The kick issuer nickname. |

<a name='M-Exiled-API-Features-Player-Kill-DamageTypes-DamageType-'></a>
### Kill(damageType) `method`

##### Summary

Kills the player.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| damageType | [DamageTypes.DamageType](#T-DamageTypes-DamageType 'DamageTypes.DamageType') | The [DamageType](#T-DamageTypes-DamageType 'DamageTypes.DamageType') that will kill the player. |

<a name='M-Exiled-API-Features-Player-RemoteAdminMessage-System-String,System-Boolean,System-String-'></a>
### RemoteAdminMessage(message,success,pluginName) `method`

##### Summary

Sends a message to the player's Remote Admin console.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |
| success | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether the message should be highlighted as success or not. |
| pluginName | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The name of the plugin. |

<a name='M-Exiled-API-Features-Player-RemoveItem-Inventory-SyncItemInfo-'></a>
### RemoveItem(item) `method`

##### Summary

Removes an item from the player's inventory.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| item | [Inventory.SyncItemInfo](#T-Inventory-SyncItemInfo 'Inventory.SyncItemInfo') | The item to be removed. |

<a name='M-Exiled-API-Features-Player-RemoveItem'></a>
### RemoveItem() `method`

##### Summary

Removes the held item from the player's inventory.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Player-ResetInventory-System-Collections-Generic-List{Inventory-SyncItemInfo}-'></a>
### ResetInventory(newItems) `method`

##### Summary

Resets the player's inventory to the provided list of items, clearing any items they already possess.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| newItems | [System.Collections.Generic.List{Inventory.SyncItemInfo}](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.List 'System.Collections.Generic.List{Inventory.SyncItemInfo}') | The new items that have to be added to the inventory. |

<a name='M-Exiled-API-Features-Player-SendConsoleMessage-System-String,System-String-'></a>
### SendConsoleMessage(message,color) `method`

##### Summary

Sends a console message to the player's console.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |
| color | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message color. |

<a name='M-Exiled-API-Features-Player-SendConsoleMessage-Exiled-API-Features-Player,System-String,System-String-'></a>
### SendConsoleMessage(target,message,color) `method`

##### Summary

Sends a console message to a [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| target | [Exiled.API.Features.Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') | The message target. |
| message | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message to be sent. |
| color | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The message color. |

<a name='M-Exiled-API-Features-Player-SetAmmo-Exiled-API-Enums-AmmoType,System-UInt32-'></a>
### SetAmmo(ammoType,amount) `method`

##### Summary

Sets the amount of a specified [AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| ammoType | [Exiled.API.Enums.AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType') | The [AmmoType](#T-Exiled-API-Enums-AmmoType 'Exiled.API.Enums.AmmoType') to be set. |
| amount | [System.UInt32](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.UInt32 'System.UInt32') | The amount of ammo to be set. |

<a name='M-Exiled-API-Features-Player-SetCamera-System-UInt16-'></a>
### SetCamera(id) `method`

##### Summary

Sets the 079 camera, if the player is SCP-079.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| id | [System.UInt16](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.UInt16 'System.UInt16') | Camera ID. |

<a name='M-Exiled-API-Features-Player-SetRank-System-String,UserGroup-'></a>
### SetRank(name,group) `method`

##### Summary

Sets the player's rank.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The rank name to be set. |
| group | [UserGroup](#T-UserGroup 'UserGroup') | The group to be set. |

<a name='M-Exiled-API-Features-Player-SetRole-RoleType,System-Boolean,System-Boolean-'></a>
### SetRole(newRole,lite,isEscaped) `method`

##### Summary

Sets the player's [RoleType](#T-RoleType 'RoleType').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| newRole | [RoleType](#T-RoleType 'RoleType') | The new [RoleType](#T-RoleType 'RoleType') to be set. |
| lite | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether it should preserve the position and inventory after changing the role or not. |
| isEscaped | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether the player is escaped or not. |

<a name='M-Exiled-API-Features-Player-ShowTag-System-Boolean-'></a>
### ShowTag(isGlobal) `method`

##### Summary

Shows the player's tag.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| isGlobal | [System.Boolean](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Boolean 'System.Boolean') | Indicates whether or not the tag will be shown globally or not. |

<a name='T-Exiled-API-Features-Plugin'></a>
## Plugin `type`

##### Namespace

Exiled.API.Features

##### Summary

Expose how a plugin has to be made.

<a name='P-Exiled-API-Features-Plugin-Config'></a>
### Config `property`

##### Summary

Gets the plugin [IConfig](#T-Exiled-API-Interfaces-IConfig 'Exiled.API.Interfaces.IConfig').

<a name='P-Exiled-API-Features-Plugin-Name'></a>
### Name `property`

##### Summary

Gets the plugin name.

<a name='P-Exiled-API-Features-Plugin-RequiredExiledVersion'></a>
### RequiredExiledVersion `property`

##### Summary

Gets the required version of EXILED to run the plugin without bugs or incompatibilities.

<a name='P-Exiled-API-Features-Plugin-Version'></a>
### Version `property`

##### Summary

Gets the plugin version.

<a name='M-Exiled-API-Features-Plugin-OnDisabled'></a>
### OnDisabled() `method`

##### Summary

Fired after disabling the plugin.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Plugin-OnEnabled'></a>
### OnEnabled() `method`

##### Summary

Fired after enabling the plugin.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Plugin-OnReloaded'></a>
### OnReloaded() `method`

##### Summary

Fired after reloading the plugin.

##### Parameters

This method has no parameters.

<a name='T-Exiled-API-Extensions-Reflection'></a>
## Reflection `type`

##### Namespace

Exiled.API.Extensions

##### Summary

A set of extensions for [Type](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Type 'System.Type').

<a name='M-Exiled-API-Extensions-Reflection-InvokeStaticMethod-System-Type,System-String,System-Object[]-'></a>
### InvokeStaticMethod(type,methodName,param) `method`

##### Summary

Invoke a static method.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| type | [System.Type](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Type 'System.Type') | The method type. |
| methodName | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The method name. |
| param | [System.Object[]](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Object[] 'System.Object[]') | The method parameters. |

<a name='T-Exiled-API-Extensions-Role'></a>
## Role `type`

##### Namespace

Exiled.API.Extensions

##### Summary

A set of extensions for [RoleType](#T-RoleType 'RoleType').

<a name='M-Exiled-API-Extensions-Role-GetTeam-RoleType-'></a>
### GetTeam(roleType) `method`

##### Summary

Get the [Team](#T-Team 'Team') of the given [RoleType](#T-RoleType 'RoleType').

##### Returns

[Team](#T-Team 'Team').

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| roleType | [RoleType](#T-RoleType 'RoleType') | Role. |

<a name='T-Exiled-API-Features-Room'></a>
## Room `type`

##### Namespace

Exiled.API.Features

##### Summary

The in-game room.

<a name='M-Exiled-API-Features-Room-#ctor-System-String,UnityEngine-Transform,UnityEngine-Vector3-'></a>
### #ctor(name,transform,position) `constructor`

##### Summary

Initializes a new instance of the [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room') class.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| name | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The room name. |
| transform | [UnityEngine.Transform](#T-UnityEngine-Transform 'UnityEngine.Transform') | The room transform. |
| position | [UnityEngine.Vector3](#T-UnityEngine-Vector3 'UnityEngine.Vector3') | The room position. |

<a name='P-Exiled-API-Features-Room-Name'></a>
### Name `property`

##### Summary

Gets or sets the [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room') name.

<a name='P-Exiled-API-Features-Room-Players'></a>
### Players `property`

##### Summary

Gets a [IEnumerable\`1](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Collections.Generic.IEnumerable`1 'System.Collections.Generic.IEnumerable`1') of [Player](#T-Exiled-API-Features-Player 'Exiled.API.Features.Player') in the [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room').

<a name='P-Exiled-API-Features-Room-Position'></a>
### Position `property`

##### Summary

Gets or sets the [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room') position.

<a name='P-Exiled-API-Features-Room-Transform'></a>
### Transform `property`

##### Summary

Gets the [Room](#T-Exiled-API-Features-Room 'Exiled.API.Features.Room')[Transform](#T-UnityEngine-Transform 'UnityEngine.Transform').

<a name='P-Exiled-API-Features-Room-Zone'></a>
### Zone `property`

##### Summary

Gets the [ZoneType](#T-Exiled-API-Enums-ZoneType 'Exiled.API.Enums.ZoneType') in which the room is located.

<a name='T-Exiled-API-Features-Round'></a>
## Round `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to handle the round more easily.

<a name='P-Exiled-API-Features-Round-ElapsedTime'></a>
### ElapsedTime `property`

##### Summary

Gets the time elapsed from the start of the round.

<a name='P-Exiled-API-Features-Round-IsLobbyLocked'></a>
### IsLobbyLocked `property`

##### Summary

Gets or sets a value indicating whether the lobby is locked or not.

<a name='P-Exiled-API-Features-Round-IsLocked'></a>
### IsLocked `property`

##### Summary

Gets or sets a value indicating whether the round is locked or not.

<a name='P-Exiled-API-Features-Round-IsStarted'></a>
### IsStarted `property`

##### Summary

Gets a value indicating whether the round is started or not.

<a name='P-Exiled-API-Features-Round-StartedTime'></a>
### StartedTime `property`

##### Summary

Gets the start time of the round.

<a name='T-Exiled-API-Features-Scp914'></a>
## Scp914 `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to use the Scp914 machine more easily.

<a name='P-Exiled-API-Features-Scp914-ConfigMode'></a>
### ConfigMode `property`

##### Summary

Gets or sets SCP-914 config mode.

<a name='P-Exiled-API-Features-Scp914-IntakeBooth'></a>
### IntakeBooth `property`

##### Summary

Gets the intake booth [Transform](#T-UnityEngine-Transform 'UnityEngine.Transform').

<a name='P-Exiled-API-Features-Scp914-IsWorking'></a>
### IsWorking `property`

##### Summary

Gets a value indicating whether the SCP-914 is working or not.

<a name='P-Exiled-API-Features-Scp914-KnobStatus'></a>
### KnobStatus `property`

##### Summary

Gets or sets SCP-914 [Scp914Knob](#T-Scp914-Scp914Knob 'Scp914.Scp914Knob').

<a name='P-Exiled-API-Features-Scp914-OutputBooth'></a>
### OutputBooth `property`

##### Summary

Gets the output booth [Transform](#T-UnityEngine-Transform 'UnityEngine.Transform').

<a name='P-Exiled-API-Features-Scp914-Recipes'></a>
### Recipes `property`

##### Summary

Gets or sets SCP-914 recipes.

<a name='M-Exiled-API-Features-Scp914-Start'></a>
### Start() `method`

##### Summary

Starts the SCP-914.

##### Parameters

This method has no parameters.

<a name='T-Exiled-API-Features-Server'></a>
## Server `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to work with the server code more easily .

<a name='P-Exiled-API-Features-Server-BanPlayer'></a>
### BanPlayer `property`

##### Summary

Gets the cached [BanPlayer](#P-Exiled-API-Features-Server-BanPlayer 'Exiled.API.Features.Server.BanPlayer') component.

<a name='P-Exiled-API-Features-Server-Broadcast'></a>
### Broadcast `property`

##### Summary

Gets the cached [Broadcast](#P-Exiled-API-Features-Server-Broadcast 'Exiled.API.Features.Server.Broadcast') component.

<a name='P-Exiled-API-Features-Server-FriendlyFire'></a>
### FriendlyFire `property`

##### Summary

Gets or sets a value indicating whether friendly fire is enabled or not.

<a name='P-Exiled-API-Features-Server-Host'></a>
### Host `property`

##### Summary

Gets the player's host of the server.

<a name='P-Exiled-API-Features-Server-Name'></a>
### Name `property`

##### Summary

Gets or sets the name of the server.

<a name='P-Exiled-API-Features-Server-Port'></a>
### Port `property`

##### Summary

Gets or sets the port of the server.

<a name='P-Exiled-API-Features-Server-SendSpawnMessage'></a>
### SendSpawnMessage `property`

##### Summary

Gets the cached [SendSpawnMessage](#P-Exiled-API-Features-Server-SendSpawnMessage 'Exiled.API.Features.Server.SendSpawnMessage')[MethodInfo](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.Reflection.MethodInfo 'System.Reflection.MethodInfo').

<a name='T-Exiled-API-Enums-Side'></a>
## Side `type`

##### Namespace

Exiled.API.Enums

##### Summary

In which side a certain [RoleType](#T-RoleType 'RoleType') belongs.

<a name='F-Exiled-API-Enums-Side-ChaosInsurgency'></a>
### ChaosInsurgency `constants`

##### Summary

Chaos Insurgency team.
Contains [ClassD](#F-RoleType-ClassD 'RoleType.ClassD') and [ChaosInsurgency](#F-RoleType-ChaosInsurgency 'RoleType.ChaosInsurgency').

<a name='F-Exiled-API-Enums-Side-Mtf'></a>
### Mtf `constants`

##### Summary

Mobile Task Forces team.
Contains [Scientist](#F-RoleType-Scientist 'RoleType.Scientist'), [FacilityGuard](#F-RoleType-FacilityGuard 'RoleType.FacilityGuard'), [NtfCadet](#F-RoleType-NtfCadet 'RoleType.NtfCadet'), [NtfLieutenant](#F-RoleType-NtfLieutenant 'RoleType.NtfLieutenant'),
[NtfCommander](#F-RoleType-NtfCommander 'RoleType.NtfCommander') and [NtfScientist](#F-RoleType-NtfScientist 'RoleType.NtfScientist').

<a name='F-Exiled-API-Enums-Side-None'></a>
### None `constants`

##### Summary

[RIP](#F-Team-RIP 'Team.RIP').

<a name='F-Exiled-API-Enums-Side-Scp'></a>
### Scp `constants`

##### Summary

The same as [SCP](#F-Team-SCP 'Team.SCP').

<a name='F-Exiled-API-Enums-Side-Tutorial'></a>
### Tutorial `constants`

##### Summary

[TUT](#F-Team-TUT 'Team.TUT').

<a name='T-Exiled-API-Extensions-String'></a>
## String `type`

##### Namespace

Exiled.API.Extensions

##### Summary

A set of extensions for [String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String').

<a name='M-Exiled-API-Extensions-String-ExtractCommand-System-String-'></a>
### ExtractCommand(commandLine) `method`

##### Summary

Extract command name and arguments from a [String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String').

##### Returns

Returns a [ValueTuple](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.ValueTuple 'System.ValueTuple') containing the exctracted command name and arguments.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| commandLine | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The [String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') to extract from. |

<a name='M-Exiled-API-Extensions-String-GetDistance-System-String,System-String-'></a>
### GetDistance(firstString,secondString) `method`

##### Summary

Compute the distance between two [String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String').

##### Returns

Returns the distance between the two strings.

##### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| firstString | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The first string to be compared. |
| secondString | [System.String](http://msdn.microsoft.com/query/dev14.query?appId=Dev14IDEF1&l=EN-US&k=k:System.String 'System.String') | The second string to be compared. |

<a name='T-Exiled-API-Features-Warhead'></a>
## Warhead `type`

##### Namespace

Exiled.API.Features

##### Summary

A set of tools to work with the warhead code more easily.

<a name='P-Exiled-API-Features-Warhead-Controller'></a>
### Controller `property`

##### Summary

Gets the cached [AlphaWarheadController](#T-AlphaWarheadController 'AlphaWarheadController') component.

<a name='P-Exiled-API-Features-Warhead-DetonationTimer'></a>
### DetonationTimer `property`

##### Summary

Gets or sets the warhead detonation timer.

<a name='P-Exiled-API-Features-Warhead-IsDetonated'></a>
### IsDetonated `property`

##### Summary

Gets a value indicating whether the warhead has already been detonated or not.

<a name='P-Exiled-API-Features-Warhead-IsInProgress'></a>
### IsInProgress `property`

##### Summary

Gets a value indicating whether the warhead detonation is in progress or not.

<a name='P-Exiled-API-Features-Warhead-IsWarheadLocked'></a>
### IsWarheadLocked `property`

##### Summary

Gets or sets a value indicating whether the warhead can be disabled or not.

<a name='P-Exiled-API-Features-Warhead-LeverStatus'></a>
### LeverStatus `property`

##### Summary

Gets or sets a value indicating whether the warhead lever is enabled or not.

<a name='P-Exiled-API-Features-Warhead-SitePanel'></a>
### SitePanel `property`

##### Summary

Gets the cached [AlphaWarheadNukesitePanel](#T-AlphaWarheadNukesitePanel 'AlphaWarheadNukesitePanel') component.

<a name='M-Exiled-API-Features-Warhead-Detonate'></a>
### Detonate() `method`

##### Summary

Detonates the warhead.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Warhead-Start'></a>
### Start() `method`

##### Summary

Starts the warhead countdown.

##### Parameters

This method has no parameters.

<a name='M-Exiled-API-Features-Warhead-Stop'></a>
### Stop() `method`

##### Summary

Stops the warhead.

##### Parameters

This method has no parameters.

<a name='T-Exiled-API-Enums-ZoneType'></a>
## ZoneType `type`

##### Namespace

Exiled.API.Enums

##### Summary

Facility zone types.

<a name='F-Exiled-API-Enums-ZoneType-Entrance'></a>
### Entrance `constants`

##### Summary

The Entrance Zone.

<a name='F-Exiled-API-Enums-ZoneType-HeavyContainment'></a>
### HeavyContainment `constants`

##### Summary

The Heavy Containment Zone.

<a name='F-Exiled-API-Enums-ZoneType-LightContainment'></a>
### LightContainment `constants`

##### Summary

The Light Containment Zone.

<a name='F-Exiled-API-Enums-ZoneType-Surface'></a>
### Surface `constants`

##### Summary

The Surface Zone.

<a name='F-Exiled-API-Enums-ZoneType-Unspecified'></a>
### Unspecified `constants`

##### Summary

An unknown zone.
