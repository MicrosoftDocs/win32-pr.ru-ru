---
description: 'Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
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
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089142"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>Метод IMpeg2PsiParser:: Жетрекордпрограмнумбер

Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.

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

 

 




