---
title: Метод Креатеусердисктемплате класса Win32_TSSessionDirectory
description: Создает шаблон диска пользователя.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Креатеусердисктемплате
- Службы удаленных рабочих столов метода Креатеусердисктемплате, класс Win32_TSSessionDirectory
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов, метод Креатеусердисктемплате
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135331"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Метод Креатеусердисктемплате \_ класса Win32 тссессиондиректори

Создает шаблон диска пользователя.

## <a name="syntax"></a>Синтаксис


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Усердискссторажеурл* \[ окне\]
</dt> <dd>

Расположение общей папки, в которой хранятся все диски пользователей.

</dd> <dt>

*Усердискмакссизеингб* \[ окне\]
</dt> <dd>

Максимальный размер (в гигабайтах) для всех дисков пользователей.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





