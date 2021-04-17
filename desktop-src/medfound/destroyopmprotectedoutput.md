---
description: Освобождает защищенный выходной объект.
ms.assetid: e9b09fd7-9db2-4189-b347-55f5fede2f80
title: Функция Дестройопмпротектедаутпут
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: 0a7ce8551cc5e01e7a2801dd129d5dc6903af697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682372"
---
# <a name="destroyopmprotectedoutput-function"></a>Функция Дестройопмпротектедаутпут

> [!IMPORTANT]
> Эта функция используется [выходными данными диспетчера защиты](output-protection-manager.md) (ОПМ) для доступа к функциям видеодрайвера. Приложения не должны вызывать эту функцию.

 

Освобождает защищенный выходной объект.

## <a name="syntax"></a>Синтаксис


```C++
NTSTATUS WINAPI DestroyOPMProtectedOutput(
  _In_ OPM_PROTECTED_OUTPUT_HANDLE opoOPMProtectedOutput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*опупмпротектедаутпут* \[ окне\]
</dt> <dd>

Маркер защищенного выходного объекта. Этот маркер получается путем вызова [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md).

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

 

 
