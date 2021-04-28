---
description: 'Метод IMpeg2PsiParser:: Жетпмтверсионнумбер. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'Метод IMpeg2PsiParser:: Жетпмтверсионнумбер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084562"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>Метод IMpeg2PsiParser:: Жетпмтверсионнумбер

Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.

`GetPmtVersionNumber`Метод извлекает \_ поле номера версии из УКАЗАННОГО типа ПЛТ. Номер версии увеличивается при каждом изменении определения программы.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*впрограмнумбер* \[ окне\]
</dt> <dd>

Указывает \_ поле номера программы программы, как указано в Pat.

</dd> <dt>

*ппмтверсион* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает \_ поле номера версии.

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

 

 




