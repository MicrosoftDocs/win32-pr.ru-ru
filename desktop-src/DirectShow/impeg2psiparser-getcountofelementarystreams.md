---
description: Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'Метод IMpeg2PsiParser:: Жеткаунтофелементаристреамс'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672977"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>Метод IMpeg2PsiParser:: Жеткаунтофелементаристреамс

Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.

`GetCountOfElementaryStreams`Метод получает количество простейших потоков в указанной программе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*впрограмнумбер* \[ окне\]
</dt> <dd>

Указывает \_ поле номера программы для программы, как указано в Pat.

</dd> <dt>

*пввал* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает количество простейших потоков в программе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает значение **HRESULT** . Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Чтобы получить номер программы, используйте метод **жетрекордпрограмнумбер** .

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser:: Жетрекордпрограмнумбер**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Образец фильтра средства синтаксического анализа PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




