---
description: Указывает, поддерживает ли Media Foundationное преобразование (MFT) трехмерное видео стереоскопик.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Атрибут MFT_SUPPORT_3DVIDEO (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da60bac92d1274f9d9a6624e247fc24d122ec26eabc103ad2d43477ae8f6b64b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776994"
---
# <a name="mft_support_3dvideo-attribute"></a>Таблица MFT \_ поддерживает \_ атрибут 3DVIDEO

Указывает, поддерживает ли Media Foundationное преобразование (MFT) трехмерное видео стереоскопик.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Remarks

Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT. Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Значение этого атрибута по умолчанию равно **false**. Рассматривайте этот атрибут как доступный только для чтения. Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                              |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




