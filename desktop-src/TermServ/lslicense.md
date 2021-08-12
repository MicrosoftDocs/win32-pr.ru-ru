---
title: Структура Лслиценсе
description: Содержит сведения о конкретной лицензии службы удаленных рабочих столов.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов структуры Лслиценсе
- службы удаленных рабочих столов указателя структуры Лплслиценсе
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ea276b1b1217505a7bb44e1d70dd58d53eb57933d755ed9f79100abc177c3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605417"
---
# <a name="lslicense-structure"></a>Структура Лслиценсе

Содержит сведения о конкретной лицензии службы удаленных рабочих столов.

> [!Note]  
> Эта структура не определена ни в одном файле заголовка. Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.

 

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Версия лицензии.

</dd> <dt>

**двлиценсеид**
</dt> <dd>

Идентификатор лицензии.

</dd> <dt>

**двкэйпаккид**
</dt> <dd>

Идентификатор [**лскэйпакк**](lskeypack.md) , который содержит лицензию.

</dd> <dt>

**сзвид**
</dt> <dd>

Идентификатор оборудования клиента подключение к удаленному рабочему столу (RDC), который выдал лицензию.

</dd> <dt>

**сзмачиненаме**
</dt> <dd>

Имя клиента подключение к удаленному рабочему столу (RDC), который выдал лицензию.

</dd> <dt>

**сзусернаме**
</dt> <dd>

Имя пользователя, который выдал лицензию.

</dd> <dt>

**двцертсериаллиценсе**
</dt> <dd>

Зарезервировано для последующего использования.

</dd> <dt>

**двлиценсесериалнумбер**
</dt> <dd>

Серийный номер лицензии.

</dd> <dt>

**фтиссуедате**
</dt> <dd>

Дата выдачи лицензии.

</dd> <dt>

**фтекспиредате**
</dt> <dd>

Дата истечения срока действия лицензии.

</dd> <dt>

**уклиценсестатус**
</dt> <dd>

Текущее состояние лицензии.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**лскэйпакк**](lskeypack.md)
</dt> <dt>

[**тлслиценсинумбегин**](tlslicenseenumbegin.md)
</dt> <dt>

[**тлслиценсинумнекст**](tlslicenseenumnext.md)
</dt> <dt>

[**тлслиценсинуменд**](tlslicenseenumend.md)
</dt> </dl>

 

 





