---
description: Отменяет все ожидающие операции ввода и вывода (I/O), выданные вызывающим потоком для указанного файла.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Функция Канцелио (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 900a47d51df882ce1f2931489ea93b5e3b4c498b8d5cc0f35e521e015e12c1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075344"
---
# <a name="cancelio-function"></a>Функция Канцелио

Отменяет все ожидающие операции ввода и вывода (I/O), выданные вызывающим потоком для указанного файла. Функция не отменяет операции ввода-вывода, которые другие потоки выдают для маркера файла.

Чтобы отменить операции ввода-вывода из другого потока, используйте функцию [**канцелиоекс**](cancelioex-func.md) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*hFile* \[ окне\]
</dt> <dd>

Маркер файла.

Функция отменяет все ожидающие операции ввода-вывода для этого обработчика файлов.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполняется успешно, возвращается ненулевое значение. Успешно запрошена операция отмены для всех ожидающих операций ввода-вывода, выданных вызывающим потоком для указанного маркера файла. Поток может использовать функцию [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) , чтобы определить, когда завершаются операции ввода-вывода.

Если функция завершается ошибкой, возвращаемое значение равно нулю (0). Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Remarks

Если для указанного маркера файла выполняются ожидающие выполнения операции ввода-вывода и они выдаются вызывающим потоком, функция **канцелио** отменяет их. **Канцелио** отменяет только что необработанные операции ввода-вывода для маркера, он не изменяет состояние маркера. Это означает, что вы не можете полагаться на состояние маркера, так как вы не можете определить, завершилась ли операция успешно или отменена.

Операции ввода-вывода должны выдаваться как перекрывающиеся операции ввода-вывода. Если это не так, операции ввода-вывода не возвращают, чтобы разрешить потоку вызывать функцию **канцелио** . Вызов функции **канцелио** с маркером файла, который не открыт с **\_ \_ перекрытием флага файла** , не выполняет никаких действий.

Все операции ввода-вывода, отмененные с ошибкой, **\_ \_ прерываются**, и все уведомления о завершении операций ввода-вывода выполняются обычным образом.

в Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.



| Технология                                           | Поддерживается      |
|------------------------------------------------------|----------------|
| Протокол SMB 3,0<br/>   | Да<br/> |
| Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)<br/>        | Да<br/> |
| SMB 3,0 с масштабируемыми файловыми ресурсами (SO)<br/>   | Да<br/> |
| Общий том кластераная файловая система (CsvFS)<br/> | Да<br/> |
| Восстанавливаемая файловая система (ReFS)<br/>              | Да<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений XP \|\]<br/>                                                                                                                                                                                                                                                       |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2003 \|\]<br/>                                                                                                                                                                                                                                              |
| Заголовок<br/>                   | <dl> <dt>иоапи. h (включает Windows. h);</dt> <dt>винбасе. h на Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 и Windows XP (включая Windows. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>См. также

<dl> <dt>

[**канцелиоекс**](cancelioex-func.md)
</dt> <dt>

[**канцелсинчронаусио**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Функции управления файлами](file-management-functions.md)
</dt> <dt>

[**локкфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**реаддиректоричанжесв**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[Синхронный и асинхронный ввод-вывод](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

