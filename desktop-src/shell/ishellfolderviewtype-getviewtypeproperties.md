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
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842705"
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

Тип: **DWORD \***

Указатель на целочисленную переменную без знака, которая получает свойства представления, которые указывают действия, выполняемые при выборе представления. Флагами могут быть любые сочетания следующих значений.

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**Сфвтфлаг \_ УВЕДОМЛЕНИЕ о \_ создании** (0x00000001)


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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




