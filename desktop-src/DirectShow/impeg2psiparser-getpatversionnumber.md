---
description: 'Метод IMpeg2PsiParser:: Жетпатверсионнумбер. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'Метод IMpeg2PsiParser:: Жетпатверсионнумбер'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 978da4c7076bcf8ffe91bc2b9a4b2077d9d3d48a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089152"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>Метод IMpeg2PsiParser:: Жетпатверсионнумбер

Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.

`GetPatVersionNumber`Метод извлекает \_ поле номера версии из Pat. Транспортный поток содержит не более одного PAT. Номер версии увеличивается каждый раз, когда изменяется информация в таблице.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппатверсион* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает \_ поле номера версии.

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

 

 




