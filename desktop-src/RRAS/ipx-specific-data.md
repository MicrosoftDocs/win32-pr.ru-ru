---
title: Структура IPX_SPECIFIC_DATA (RTM. h)
description: '\_Структура данных, относящаяся к IPX, \_ содержит данные, относящиеся к IPX.'
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- RAS структуры IPX_SPECIFIC_DATA
- RAS — указатель структуры PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988164"
---
# <a name="ipx_specific_data-structure"></a>\_Структура данных, характерная для IPX \_

\[Этот API был заменен API [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

Структура **\_ \_ данных, относящаяся к IPX** , содержит данные, относящиеся к IPX.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Флаги ФСД**
</dt> <dd>

Задает флаги, описывающие маршрут. В настоящее время этот элемент либо равен нулю, либо имеет следующее значение флага.



| Значение                                                                                                                                                                                                      | Значение                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**Глобальный IPX- \_ \_ \_ маршрут глобальной сети \_**</dt> </dl> | Указывает, что этот маршрут предназначен для глобальной сети, выделенной для всех клиентов глобальной сети.<br/> |



 

</dd> <dt>

**ФСДое \_ TickCount**
</dt> <dd>

Указывает число тактов, необходимое для достижения целевой сети. Протоколы маршрутизации, отличные от RIP, должны преобразовывать свои метрики в такты.

</dd> <dt>

**ФСД \_ хопкаунт**
</dt> <dd>

Указывает число прыжков, связанное с маршрутом.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                        |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                             |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                   |
| Header<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по диспетчеру таблиц маршрутизации версии 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Структуры диспетчера таблиц маршрутизации версии 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_маршрут IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





