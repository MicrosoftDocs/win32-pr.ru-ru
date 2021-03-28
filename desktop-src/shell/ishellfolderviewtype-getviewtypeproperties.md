---
description: Возвращает свойства представления.
title: 'Метод Ишеллфолдервиевтипе:: Жетвиевтипепропертиес'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f4368edf6eae3e6892a3d81147401e061548f6e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984624"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>Метод Ишеллфолдервиевтипе:: Жетвиевтипепропертиес

Возвращает свойства представления.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пидл* \[ окне\]
</dt> <dd>

Тип: **\_ дочерний элемент пкуитемид**

ПИДЛ.

</dd> <dt>

*пдвфлагс* \[ заполняет\]
</dt> <dd>

Введите: **DWORD \** _

Указатель на целочисленную переменную без знака, которая получает свойства представления, которые указывают действия, выполняемые при выборе представления. Флагами могут быть любые сочетания следующих значений.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>_ *Сфвтфлаг \_ уведомлять \_ CREATE** (0x00000001)


</dt> <dd>

Создать элемент представления, если нет.

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**Сфвтфлаг \_ УВЕДОМЛЕНИЕ \_ курорт** (0x00000002)


</dt> <dd>

Повторно вставьте ПИДЛ и повторите сортировку.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




