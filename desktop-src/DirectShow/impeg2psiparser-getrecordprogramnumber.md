---
description: 'метод IMpeg2PsiParser:: жетрекордпрограмнумбер. реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.'
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: e42e991fc7e288fc36dafcd167fe21ffb4983baeeb34bbb80e1bf67981e24779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083704"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер

реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.

`GetRecordProgramNumber`Метод извлекает номер программы для указанной программы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Указывает запись в PAT, определяющую программу, индексируемую от нуля.

</dd> <dt>

*пввал* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает поле "номер программы" \_ из Pat.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает значение **HRESULT** . Возможные значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Успешно.<br/> |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Образец фильтра средства синтаксического анализа PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




