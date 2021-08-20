---
description: Указывает, что был запущен Поиск.
title: 'Метод Ишеллфолдерсеарчаблекаллбакк:: Рунбегин'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback.RunBegin
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6e3ae592-a0cb-4d9d-b186-241a757da5ea
ms.openlocfilehash: 026b5b458736a0805d48dc59715a1705ecdb8557037232332767946dd05d333d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223354"
---
# <a name="ishellfoldersearchablecallbackrunbegin-method"></a>Метод Ишеллфолдерсеарчаблекаллбакк:: Рунбегин

Указывает, что был запущен Поиск.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RunBegin(
  [in] DWORD dwReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двресервед* \[ окне\]
</dt> <dd>

Тип: **DWORD**

Зарезервировано. Должен иметь значение 0.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

В ответ на этот обратный вызов приложение может включить кнопку **Отмена** , например.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                             |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




