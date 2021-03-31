---
description: Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'Метод IMpeg2PsiParser:: Жеткаунтофпрограмс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894853"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>Метод IMpeg2PsiParser:: Жеткаунтофпрограмс

Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.

`GetCountOfPrograms`Метод извлекает количество программ в транспортном потоке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пнумофпрограмс* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает количество программ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает значение HRESULT. Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Успешно.<br/> |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Образец фильтра средства синтаксического анализа PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




