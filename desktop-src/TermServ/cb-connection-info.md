---
title: Структура CB_CONNECTION_INFO (Кбклиент. h)
description: Содержит сведения о входящем запросе на подключение.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO структуры службы удаленных рабочих столов
- PCB_CONNECTION_INFO службы удаленных рабочих столов указателя на структуру
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415088"
---
# <a name="cb_connection_info-structure"></a>\_ \_ Структура сведений о СОЕДИНЕНии CB

Содержит сведения о входящем запросе на подключение. Эта структура используется с методом [**иконнектионброкерклиент:: жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**UserName**
</dt> <dd>

Имя пользователя, запросившего сеанс.

</dd> <dt>

**Доменная**
</dt> <dd>

Имя домена, членом которого является имя **пользователя** .

</dd> <dt>

**инитиалпрограм**
</dt> <dd>

Полный путь и имя файла начальной программы, которая запускается при запуске сеанса. Если начальная программа не должна запускаться, присвойте этому элементу пустую строку.

</dd> <dt>

**Ресурс**
</dt> <dd>

Значение перечисления [**\_ \_ типа ресурса CB**](cb-resource-type.md) , указывающее тип ресурса, к которому подключается входящее подключение. Если элемент **PluginName** имеет **значение NULL**, этот член используется компонентом подключение к удаленному рабочему столу Broker, чтобы определить, какой подключаемый модуль следует вызвать для определения целевого компьютера.

</dd> <dt>

**PluginName**
</dt> <dd>

Имя подключаемого модуля, вызываемого для определения целевого компьютера. Если этот параметр имеет **значение NULL**, то для определения подключаемого модуля используется член **ресурса** .

</dd> <dt>

**фармнаме**
</dt> <dd>

Имя фермы, содержащей компьютеры, один из которых будет целевым компьютером, на который будет перенаправлено подключение.

</dd> <dt>

**дввендоринфоленгс**
</dt> <dd>

Этот элемент зарезервирован для использования в будущем.

</dd> <dt>

**пвендорспеЦифиЦинфо**
</dt> <dd>

Этот элемент зарезервирован для использования в будущем.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Кбклиент. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иконнектионброкерклиент:: Жеттаржетинфо**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





