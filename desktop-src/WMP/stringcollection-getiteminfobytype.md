---
title: StringCollection. Жетитеминфобитипе, метод
description: Метод Жетитеминфобитипе извлекает значение, соответствующее указанному индексу StringCollection, имени, языку и индексу атрибута.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- Жетитеминфобитипе метод Windows Media Player
- Жетитеминфобитипе метод Windows Media Player, класс StringCollection
- Класс StringCollection Windows Media Player, метод Жетитеминфобитипе
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717855"
---
# <a name="stringcollectiongetiteminfobytype-method"></a>StringCollection. Жетитеминфобитипе, метод

Метод **жетитеминфобитипе** извлекает значение, соответствующее указанному индексу **StringCollection** , имени, языку и индексу атрибута.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), указывающее Отсчитываемый от нуля индекс элемента **StringCollection** , из которого необходимо получить атрибут.

</dd> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута.

</dd> <dt>

*языковая* \[ окне\]
</dt> <dd>

**Строка** , содержащая язык. Если задано значение null или пустая строка (""), используется текущая строка языкового стандарта. В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".

</dd> <dt>

*аттрибутеиндекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее Отсчитываемый от нуля индекс значения, извлекаемого из атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число**, **строку**, объект **метадатапиктуре** или объект **метадататекст** , как показано в следующей таблице.



| attribute                   | Возвращаемое значение                   |
|-----------------------------|--------------------------------|
| **синкстате**               | **Число** (**без знака**) |
| **WM/ \_ синхронизированы песен** | Объект **метадататекст**        |
| **WM/Picture**              | Объект **метадатапиктуре**     |
| **WM/Усервебурл**           | Объект **метадататекст**        |
| Все остальные атрибуты        | Строка                         |



 

Для атрибутов, базовое значение которых является **логическим**, этот метод возвращает строку "true" или "false".

## <a name="remarks"></a>Комментарии

Этот метод поддерживает атрибуты с несколькими значениями и атрибуты со сложными значениями. Метод **getItemInfo** не поддерживает атрибуты с несколькими или сложными значениями.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Метадатапиктуре**](metadatapicture-object.md)
</dt> <dt>

[**Объект Метадататекст**](metadatatext-object.md)
</dt> <dt>

[**StringCollection. getItemInfo**](stringcollection-getiteminfo.md)
</dt> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





