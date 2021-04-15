---
title: Метод Провисионингжобексекуте класса Win32_RDMSVirtualDesktopCollection
description: Запускает задание подготовки виртуальных рабочих столов.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингжобексекуте
- Службы удаленных рабочих столов метода Провисионингжобексекуте, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионингжобексекуте
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492762"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Провисионингжобексекуте \_ класса Win32 рдмсвиртуалдесктопколлектион

Запускает задание подготовки виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Жобинпутксмл* \[ окне\]
</dt> <dd>

Строка, содержащая сведения об инициализации в формате XML.

</dd> <dt>

*Жобгуид* \[ заполняет\]
</dt> <dd>

**Идентификатор GUID** , однозначно определяющий выполняемое задание подготовки.

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

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





