---
title: Метод Сетклиентваллпапер класса Win32_TSEnvironmentSetting
description: Метод Сетклиентваллпапер задает свойство Клиентваллпапер.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетклиентваллпапер
- Службы удаленных рабочих столов метода Сетклиентваллпапер, класс Win32_TSEnvironmentSetting
- Класс Win32_TSEnvironmentSetting службы удаленных рабочих столов, метод Сетклиентваллпапер
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b314148bf630dace88c08b532cf80d2bed68d9e41f5566a198a79eef6e52a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126858"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Метод Сетклиентваллпапер \_ класса Win32 тсенвиронментсеттинг

Метод **сетклиентваллпапер** задает свойство **клиентваллпапер** .

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Клиентваллпапер* \[ окне\]
</dt> <dd>

Флаг отключения или включения свойства **клиентваллпапер** , которое указывает, отображается ли на клиенте фоновый рисунок (или фоновый рисунок).

<dt>

<span id="0"></span>

<span id="0"></span>**0,0**


</dt> <dd>

Фоновое изображение (или фоновый рисунок) не отображается на клиенте.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Фоновое изображение (или фоновый рисунок) отображается на клиенте.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI. Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) . Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.

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

[**\_Тсенвиронментсеттинг Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

