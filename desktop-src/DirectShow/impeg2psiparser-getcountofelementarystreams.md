---
description: 'метод IMpeg2PsiParser:: жеткаунтофелементаристреамс. реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.'
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
ms.openlocfilehash: e241697884a4b665c160dc9991e4cb7f02c76f1ba32bc7a0656515faf1117a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767384"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>Метод IMpeg2PsiParser:: Жеткаунтофелементаристреамс

реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.

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



 

## <a name="remarks"></a>Remarks

Чтобы получить номер программы, используйте метод **жетрекордпрограмнумбер** .

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser:: Жетрекордпрограмнумбер**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Образец фильтра средства синтаксического анализа PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




