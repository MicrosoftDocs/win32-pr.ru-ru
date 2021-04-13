---
description: Возвращает 128-битное криптографически защищенное случайное число из защищенного выходного объекта.
ms.assetid: d5adfa5c-ae61-43d5-916d-05085abea38b
title: Функция Жетопмрандомнумбер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetOPMRandomNumber
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: f78b17dcf9ffff7a5fa26ce16e96299e5cf8386c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342452"
---
# <a name="getopmrandomnumber-function"></a>Функция Жетопмрандомнумбер

> [!IMPORTANT]
> Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера. Приложения не должны вызывать эту функцию.

 

Возвращает 128-битное криптографически защищенное случайное число из защищенного выходного объекта.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI GetOPMRandomNumber(
  _In_  OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput,
  _Out_ DXGKMDT_OPM_RANDOM_NUMBER   *prnRandomNumber
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*опупмпротектедаутпут* \[ окне\]
</dt> <dd>

Маркер защищенного выходного объекта. Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).

</dd> <dt>

*прнрандомнумбер* \[ заполняет\]
</dt> <dd>

Указатель на структуру **\_ \_ случайных \_ чисел дксгкмдт ОПМ** , которая получает случайное число.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается **состояние \_ Success**. В противном случае возвращается код ошибки **NTSTATUS** .

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта. Для вызова этой функции необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Gdi32.dll.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции ОПМ](opm-functions.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> </dl>

 

 
