---
title: Константы типа NAP (Наптипес. h)
description: Определены следующие константы NAP.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672790"
---
# <a name="nap-type-constants"></a>Константы типа NAP

> [!Note]  
> Платформа защиты доступа к сети недоступна начиная с Windows 10

 

Определены следующие константы NAP.

В Наптипес. h определены следующие константы NAP:

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**макссохаттрибутекаунт**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



Максимальное число [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) объектов типа "Длина-значение" (TLV), связанных с пакетом [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**макссохаттрибутесизе**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Максимальный размер (в байтах) объекта [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) , связанного с пакетом состояния работоспособности ([**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)).


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**миннетворксохсизе**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



Минимальный размер пакета [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) в байтах.


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**макснетворксохсизе**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Максимальный размер пакета [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) в байтах.


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**максдвордкаунтперсохаттрибуте**
</dt> <dd> <dl> <dt>

Макссохаттрибутесизе/sizeof (DWORD)
</dt> <dt>



Максимальное число значений типа DWORD, связанных с [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

Макссохаттрибутесизе/0x4
</dt> <dt>



Максимальное число IPv4-адресов, связанных с [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

Макссохаттрибутесизе/0x10
</dt> <dt>



Максимальное число IPv6-адресов, связанных с [**сохаттрибуте**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**максстрингленгс**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Максимальная длина строки, заданной структурой [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**максстрингленгсинбитес**
</dt> <dd> <dl> <dt>

(Максстрингленгс + 1) \* sizeof (WCHAR)
</dt> <dt>



Максимальная длина строки в байтах, заданной структурой [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**макссистемхеалсентитикаунт**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Максимальное число сущностей работоспособности системы, таких как SHV и SHA.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**системхеалсентитикаунт**
</dt> <dd> <dl> <dt>

\[диапазон (0, Макссистемхеалсентитикаунт)\] 
</dt> <dt>



Диапазон возможных значений для числа сущностей работоспособности системы.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**максенфорцеркаунт**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Максимальное число сущностей принудительного применения, например кекс.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**енфорцементентитикаунт**
</dt> <dd> <dl> <dt>

\[диапазон (0, Максенфорцеркаунт)\]
</dt> <dt>



Диапазон возможных значений для числа сущностей принудительного применения.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**максприватедатасизе**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



Максимальный размер (в байтах) структуры [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**максконнектионкаунтперенфорцер**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Максимальное число объектов [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , связанных с сущностью принудительного применения.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**макскачедсохкаунт**
</dt> <dd> <dl> <dt>

Макссистемхеалсентитикаунт \* максенфорцеркаунт \* максконнектионкаунтперенфорцер
</dt> <dt>



Максимальное количество кэшированных подключений SoH для всех сущностей работоспособности и принудительного применения системы.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**фрешсохрекуест**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Указывает, что [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-networksoh)из-за нового запроса, а не кэшированного запроса. Этот флаг используется агентом NAP для объекта [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) .


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**шафиксуп**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Указывает, что требуется исправление. Этот флаг используется SHA.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**фаилурекатегорикаунт**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Число категорий сбоев, содержащихся в структуре [**фаилурекатегоримаппинг**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**компоненттипинфорцементклиентсох**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Компонент является клиентом принудительного применения карантина (Кек), который отправляет пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) во время проверки подлинности подключения.

> [!Note]  
> Это значение не используется SHA и SHV.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**компоненттипинфорцементклиентрп**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Компонент — это Кек, который реализует [**инапцертрелингпарти**](inapcertrelyingparty.md) и должен взаимодействовать с сервером сертификатов работоспособности (HCS) для получения сертификата работоспособности.

> [!Note]  
> Это значение не используется SHA и SHV.

 


</dt> </dl> </dd> </dl>

Следующие константы NAP определены в Напенфорцементклиент. h.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**дефаултпротоколмакссизе**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



Максимальный размер пакета SoH (в байтах) по умолчанию.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**макспротоколмакссизе**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



Максимальный возможный размер пакета SoH в байтах.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**минпротоколмакссизе**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



Наименьший возможный максимальный размер пакета SoH в байтах. Фактический размер пакета SoH может быть меньше **минпротоколмакссизе**.


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**протоколмакссизе**
</dt> <dd> <dl> <dt>

Range (Минпротоколмакссизе, Макспротоколмакссизе)
</dt> <dt>



Диапазон возможных значений для максимального размера пакета SoH.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                                                                                                      |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>Наптипес. h; </dt> <dt>Напенфорцементклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Константы NAP**](nap-constants.md)
</dt> </dl>

 

 





