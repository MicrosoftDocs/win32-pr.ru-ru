---
description: 'метод IMpeg2PsiParser:: жетпатверсионнумбер. реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.'
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
ms.openlocfilehash: ffd03bea09fb9041b91bb214287442eb59a7101be7a8841e0d38e28bcdaf3ecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767364"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>Метод IMpeg2PsiParser:: Жетпатверсионнумбер

реализация этого метода предоставляется в виде образца кода с помощью пакета SDK для DirectShow. он не является поддерживаемым DirectShow API.

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



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Образец фильтра средства синтаксического анализа PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




