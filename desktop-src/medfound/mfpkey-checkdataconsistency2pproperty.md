---
description: Указывает, должен ли кодировщик проверять согласованность данных между проходами при выполнении двусторонней кодировки VBR. Чтение и запись.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Свойство MFPKEY_CHECKDATACONSISTENCY2P (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694532"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a>МФПКЭЙ \_ CHECKDATACONSISTENCY2P, свойство

Указывает, должен ли кодировщик проверять согласованность данных между проходами при выполнении двусторонней кодировки VBR. Чтение и запись.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

**Логическое значение VT \_**

## <a name="default-value"></a>Значение по умолчанию

**ВАРИАНТ \_ true**

## <a name="remarks"></a>Комментарии

Если оставить это свойство по умолчанию со значением **Variant \_ true**, кодировщик проверяет соответствие входных выборок между двумя проходами и завершается ошибкой, если обнаруживает несоответствие. Основной сценарий, который приводит к несоответствию, заключается в том, что входные данные поступают с устройства.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Клиент<br/> | Windows Vista или Windows 7<br/>                                                   |
| Header<br/> | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
