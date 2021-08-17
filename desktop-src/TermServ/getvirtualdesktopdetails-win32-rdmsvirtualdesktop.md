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
ms.openlocfilehash: b6ca1b552147623822ae007ca17abf8e4eaebfb149f5e80ac4760719f1ef7168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059492"
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

получает значение, указывающее, включено ли RemoteFX на виртуальном рабочем столе. **значение TRUE** , если RemoteFX включен; в противном случае — **значение false**.

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

 

 





