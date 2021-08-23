---
description: Определяет, является ли строка приложения и раздела (&\# 0034; AppName \| топикнаме&\# 0034;) использует правильный синтаксис.
ms.assetid: bcf5442b-452e-4b42-95e9-f09bf885be40
title: Функция Нддеисвалидапптопиклист (Нддеапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidAppTopicList
- NDdeIsValidAppTopicListA
- NDdeIsValidAppTopicListW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: f7b70d3e33f67c8c0a457f85df91e83e374a3ef4d0f0b1a0af1c5c41ea81c2ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611134"
---
# <a name="nddeisvalidapptopiclist-function"></a>Функция Нддеисвалидапптопиклист

\[Сетевой DDE больше не поддерживается. Nddeapi.dll имеется в Windows Vista, но все вызовы функций возвращают ндде \_ не \_ реализованы.\]

Определяет, использует ли строка приложения и раздела ("*AppName* \| *топикнаме*") правильный синтаксис.

## <a name="syntax"></a>Синтаксис


```C++
BOOL NDdeIsValidAppTopicList(
  _In_ LPTSTR targetTopic
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*таржеттопик* \[ окне\]
</dt> <dd>

Указатель на строку приложения и раздел для проверки. Этот параметр не может иметь **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если параметр *таржеттопик* имеет допустимый синтаксис, возвращаемое значение не равно нулю.

Если функция выполняется неудачно, возвращается нулевое значение.

## <a name="remarks"></a>Remarks

Эта функция также вызывается [**нддешареадд**](nddeshareadd.md) при создании общего ресурса DDE.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Заголовок<br/>                   | <dl> <dt>Нддеапи. h</dt> </dl>      |
| Библиотека<br/>                  | <dl> <dt>Нддеапи. lib</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl>    |
| Имя в кодировке Юникод и ANSI<br/>   | **Нддеисвалидапптопиклиств** (Юникод) и **нддеисвалидапптопиклиста** (ANSI)<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[общие сведения о Exchange сетевых платформа динамических данных](network-dynamic-data-exchange.md)
</dt> <dt>

[Сетевые функции DDE](network-dde-functions.md)
</dt> <dt>

[**нддешареадд**](nddeshareadd.md)
</dt> </dl>

 

 




