---
description: Возвращает несколько записей портов завершения одновременно.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Функция Жеткуеуедкомплетионстатусекс (Иоапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664433"
---
# <a name="getqueuedcompletionstatusex-function"></a>Функция Жеткуеуедкомплетионстатусекс

Возвращает несколько записей портов завершения одновременно. Он ожидает завершения ожидающих операций ввода-вывода, связанных с указанным портом завершения.

Чтобы отменять постановку пакетов завершения ввода-вывода по одному, используйте функцию [**жеткуеуедкомплетионстатус**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Комплетионпорт* \[ окне\]
</dt> <dd>

Маркер порта завершения. Чтобы создать порт завершения, используйте функцию [**CreateIoCompletionPort**](createiocompletionport.md) .

</dd> <dt>

*лпкомплетионпортентриес* \[ заполняет\]
</dt> <dd>

На входе указывает на предварительно выделенный массив [**перекрывающихся структур \_ записи**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .

На выходе получает массив [**перекрывающихся структур \_ записи**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) , содержащих записи. Число элементов массива предоставляется *улнументриесремовед*.

Число байтов, передаваемых при каждом вводе-выводе, ключ завершения, указывающий, какой файл выполняется каждый ввод-вывод, и адрес перекрывающейся структуры, используемый в каждом исходном вводе-выводе, возвращается в массиве *лпкомплетионпортентриес* .

</dd> <dt>

*улкаунт* \[ окне\]
</dt> <dd>

Максимальное число удаляемых записей.

</dd> <dt>

*улнументриесремовед* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает число фактически удаленных записей.

</dd> <dt>

*dwMilliseconds* \[ окне\]
</dt> <dd>

Время в миллисекундах, в течение которого вызывающая сторона ожидает отображения пакета завершения в порте завершения. Если пакет завершения не отображается в течение заданного времени, функция истечет время ожидания и возвратит **значение false**.

Если *dwMilliseconds* имеет **бесконечное** значение (0xFFFFFFFF), функция никогда не будет исключаться. Если *dwMilliseconds* равен нулю, а операция ввода-вывода для выхода из очереди отсутствует, функция будет немедленно истечет.

</dd> <dt>

*фалертабле* \[ окне\]
</dt> <dd>

Если этот параметр имеет **значение false**, функция не возвращает результат, пока не истечет время ожидания или не будет получена запись.

Если параметр имеет **значение true** и отсутствуют доступные записи, функция выполняет предупреждение. Поток возвращается, когда система помещает в очередь подпрограммы завершения ввода-вывода или APC в поток, а поток выполняет функцию.

Подпрограммы завершения помещаются в очередь, когда функция [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) или [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) , в которой она была указана, была завершена, а вызывающий поток — это поток, который инициировал операцию. Компания APC помещается в очередь при вызове [**куеуеусерапк**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ненулевое **значение (true**) в случае успешного или нулевого значения (**false**) в противном случае.

Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Комментарии

Эта функция связывает поток с указанным портом завершения. Поток может быть связан не более чем с одним портом завершения.

Эта функция возвращает **значение true** , если по крайней мере один ожидающий ввод-вывод завершен, но возможно, что произошел сбой одной или нескольких операций ввода-вывода. Обратите внимание, что пользователь этой функции может проверить список возвращенных записей в параметре *лпкомплетионпортентриес* , чтобы определить, какие из них соответствуют любым возможным операциям ввода-вывода, просмотрев состояние, содержащееся в элементе **лповерлаппед** в каждой [**перекрывающейся \_ записи**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).

Эта функция возвращает **значение false** , если ни одна операция ввода-вывода не была выведена из очереди. Обычно это означает, что при обработке параметров для этого вызова произошла ошибка или маркер *комплетионпорт* был закрыт или в противном случае является недопустимым. Функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) предоставляет расширенные сведения об ошибке.

Если вызов [**жеткуеуедкомплетионстатусекс**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) завершается сбоем из-за закрытия связанного с ним маркера, функция возвращает **значение false** , а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвратит **ошибку No \_ \_ Wait \_ 0**.

Серверные приложения могут иметь несколько потоков, вызывающих функцию **жеткуеуедкомплетионстатусекс** для одного и того же порта завершения. По мере завершения операций ввода-вывода они помещаются в очередь на этот порт в порядке "первым пов первом выходе". Если поток активно ожидает этого вызова, один или несколько запросов, помещенных в очередь, завершают вызов только для этого потока.

Дополнительные сведения о теории портов завершения ввода-вывода, использовании и связанных функциях см. в разделе [порты завершения ввода-вывода](i-o-completion-ports.md).

В Windows 8 и Windows Server 2012 эта функция поддерживается следующими технологиями.



| Технология                                           | Поддерживается      |
|------------------------------------------------------|----------------|
| Протокол SMB 3,0<br/>   | Да<br/> |
| Прозрачная отработка отказа SMB 3,0 (ОТРАБОТКА отказа)<br/>        | Да<br/> |
| SMB 3,0 с масштабируемыми файловыми ресурсами (SO)<br/>   | Да<br/> |
| Общий том кластераная файловая система (CsvFS)<br/> | Да<br/> |
| Восстанавливаемая файловая система (ReFS)<br/>              | Да<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                                                                                                                                                                                                   |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                                                                                                                                                                                                             |
| Header<br/>                   | <dl> <dt>Иоапи. h (включение Windows. h); </dt> <dt>Винбасе. h в Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista (включая Windows. h)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

**Обзорные разделы**
</dt> <dt>

[Функции управления файлами](file-management-functions.md)
</dt> <dt>

[Порты завершения ввода-вывода](i-o-completion-ports.md)
</dt> <dt>

[Использование заголовков Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Функции**
</dt> <dt>

[**коннектнамедпипе**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**жеткуеуедкомплетионстатусекс**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**локкфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**трансактнамедпипе**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**ваиткоммевент**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

