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
ms.openlocfilehash: 0367e02dd8b0a46304538a2e5830e101eb9573e6548383fbae617a856df83621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790752"
---
# <a name="ipx_specific_data-structure"></a>\_Структура данных, характерная для IPX \_

\[этот api был заменен api [диспетчера таблиц маршрутизации версии 2](about-routing-table-manager-version-2.md) и не будет доступен за пределами Windows Server 2003. Приложения должны использовать API диспетчера таблиц маршрутизации версии 2.\]

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
| Заголовок<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Справочник по диспетчеру таблиц маршрутизации версии 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Структуры диспетчера таблиц маршрутизации версии 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_маршрут IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





