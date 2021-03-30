---
description: Извлекает значение, определяющее, является ли указанный в памяти или на диске динамический код .NET CRL доверенным для политики Device Guard.
ms.assetid: 9C12894D-98AF-4408-A11A-865E4DA1DA68
title: Функция Влдпкуеридинамиккодетруст (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpQueryDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 1b9b3cc30f5a02ae86fd8a30043a9ab417ec1ac7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538753"
---
# <a name="wldpquerydynamiccodetrust-function"></a>Функция Влдпкуеридинамиккодетруст

Извлекает значение, определяющее, является ли указанный в памяти или на диске динамический код .NET CRL доверенным для политики Device Guard.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT WINAPI WldpQueryDynamicCodeTrust(
   _When_(baseImage != NULL, _In_opt_)
    _When_(baseImage == NULL, _In_)
    HANDLE                                                 fileHandle,
   _When_(fileHandle == NULL, _In_reads_bytes_opt_(imageSize))
    _When_(fileHandle != NULL, _In_reads_bytes_(imageSize))
    PVOID  baseImage,
   _In_ ULONG                                                                                                                         ImageSize
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*fileHandle* 
</dt> <dd>

Обработчик файла динамического кода на диске для проверки. Если *fileHandle* имеет значение, отличное от **null**, *басеимаже* должно иметь **значение NULL**.

</dd> <dt>

*басеимаже* 
</dt> <dd>

Указатель на проверяемый файл PE в памяти. Если *басеимаже* имеет значение, отличное от **null**, *FileHandle* должно иметь **значение NULL**.

</dd> <dt>

*ImageSize* 
</dt> <dd>

Если *басеимаже* имеет значение, отличное от **null**, указывает размер буфера, на который указывает *басеимаже* .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **значение \_ ОК** в случае успеха или код ошибки в противном случае.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




