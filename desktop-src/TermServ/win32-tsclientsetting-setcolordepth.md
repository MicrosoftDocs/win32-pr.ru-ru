---
title: Метод Сетколордепс класса Win32_TSClientSetting
description: Метод Сетколордепс задает свойство Clientareawidth для класса.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетколордепс
- Службы удаленных рабочих столов метода Сетколордепс, класс Win32_TSClientSetting
- Класс Win32_TSClientSetting службы удаленных рабочих столов, метод Сетколордепс
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da2c7f31ef04fdfb9dcbfee5e1ca3dcec1386a7dbd0c20824b00bdfe41ac6d48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999864"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a>Метод Сетколордепс \_ класса Win32 тсклиентсеттинг

Метод **сетколордепс** задает свойство **clientareawidth** для класса.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Clientareawidth* \[ окне\]
</dt> <dd>

Новое значение для свойства **clientareawidth** .

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

8 бит на пиксель

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

15 бит на пиксель

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

16 бит на пиксель

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

24 бита на пиксель

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5.0**


</dt> <dd>

32 бит на пиксель

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает успешное завершение, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

## <a name="remarks"></a>Remarks

файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). файлы MOF не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows Software Development Kit (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсклиентсеттинг Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

