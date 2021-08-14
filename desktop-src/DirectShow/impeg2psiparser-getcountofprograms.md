---
description: 'метод IMpeg2PsiParser:: жеткаунтофпрограмс. реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.'
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
ms.openlocfilehash: c0c5609f82db98caea02e08f1e4fbd3877eeccbae25a5e83da3ac2804577b100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398111"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>Метод IMpeg2PsiParser:: Жеткаунтофпрограмс

реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.

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

 

 




