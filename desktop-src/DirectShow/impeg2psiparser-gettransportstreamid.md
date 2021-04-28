---
description: 'Метод IMpeg2PsiParser:: Жеттранспортстреамид. Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.'
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'Метод IMpeg2PsiParser:: Жеттранспортстреамид'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: a24253b021abacf398a3a169b63bbb2f01ec2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084572"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>Метод IMpeg2PsiParser:: Жеттранспортстреамид

Реализация этого метода предоставляется в виде образца кода с помощью пакета SDK DirectShow. Это не поддерживаемый API-интерфейс DirectShow.

`GetTransportStreamId`Метод получает поле идентификатора транспортного \_ потока \_ из Pat. Это значение определяется пользователем и может использоваться для различения определенного транспортного потока от других потоков в той же сети. Транспортный поток содержит не более одного PAT.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстреамид* \[ заполняет\]
</dt> <dd>

Указатель на переменную, которая получает поле идентификатора транспортного \_ потока \_ .

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

 

 




