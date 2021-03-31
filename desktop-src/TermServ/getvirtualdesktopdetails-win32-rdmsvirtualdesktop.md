---
title: Метод Жетвиртуалдесктопдетаилс класса Win32_RDMSVirtualDesktop
description: Получение дополнительных сведений о виртуальном рабочем столе.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвиртуалдесктопдетаилс
- Службы удаленных рабочих столов метода Жетвиртуалдесктопдетаилс, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Жетвиртуалдесктопдетаилс
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491337"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Метод Жетвиртуалдесктопдетаилс \_ класса Win32 рдмсвиртуалдесктоп

Получение дополнительных сведений о виртуальном рабочем столе.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рамсизеинмб* \[ заполняет\]
</dt> <dd>

Получает объем ОЗУ, назначенный виртуальному рабочему столу, в байтах.

</dd> <dt>

*Ремотефксенаблед* \[ заполняет\]
</dt> <dd>

Получает значение, указывающее, включено ли RemoteFX на виртуальном рабочем столе. **Значение true** , если RemoteFX включен. в противном случае — **значение false**.

</dd> <dt>

*OSVersion* \[ заполняет\]
</dt> <dd>

Получает версию ОС виртуального рабочего стола.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсвиртуалдесктоп Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





