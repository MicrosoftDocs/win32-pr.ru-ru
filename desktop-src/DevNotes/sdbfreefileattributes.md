---
description: Освобождает указанные данные атрибута файла.
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: Функция Сдбфрифилеаттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7e99180198f8f23ba6b6872502710b2af28aaff3999a9f315c33ef2d1874d987
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103674"
---
# <a name="sdbfreefileattributes-function"></a>Функция Сдбфрифилеаттрибутес

Освобождает указанные данные атрибута файла.

## <a name="syntax"></a>Синтаксис


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфилеаттрибутес* \[ окне\]
</dt> <dd>

Структура [**аттринфо**](attrinfo.md) , возвращаемая функцией [**сдбжетфилеаттрибутес**](sdbgetfileattributes.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Функция возвращает **true** при успешном выполнении или **false** в случае сбоя.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**сдбжетфилеаттрибутес**](sdbgetfileattributes.md)
</dt> </dl>

 

 




