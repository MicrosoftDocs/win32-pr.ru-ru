---
description: Этот API предназначен только для внутреннего использования и не должен использоваться в коде.
ms.assetid: 836A7515-8C22-4032-9E99-F89B32C21685
title: Функция Аписеткуеряписетпресенце (Apiquery. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApiSetQueryApiSetPresence
api_type:
- DllExport
api_location:
- api-ms-win-core-apiquery-l1-1-0.dll
- ntdll.dll
ms.openlocfilehash: 738a69b0d08f7e619dbd64229d0c13b2ae7dfaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664720"
---
# <a name="apisetqueryapisetpresence-function"></a>Функция Аписеткуеряписетпресенце

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Этот API предназначен только для внутреннего использования и не должен использоваться в коде.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI ApiSetQueryApiSetPresence(
  _In_  PCUNICODE_STRING Namespace,
  _Out_ PBOOLEAN         Present
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Пространство имен* \[ окне\]
</dt> <dd></dd> <dt>

*Имеется* \[ заполняет\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                                                                                                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                                                                                                                                  |
| Header<br/>                   | <dl> <dt>Apiquery. h</dt> </dl>                                                                                                                 |
| Библиотека<br/>                  | <dl> <dt>API-MS-Win-Core-apiquery-L1. lib; </dt> <dt>API-MS-Win-Core-apiquery-L1-1 -0. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Api-ms-win-core-apiquery-l1-1-0.dll</dt> </dl>                                                                                        |



 

 




