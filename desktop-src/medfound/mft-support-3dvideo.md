---
description: Указывает, поддерживает ли Media Foundationное преобразование (MFT) трехмерное видео стереоскопик.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Атрибут MFT_SUPPORT_3DVIDEO (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701803"
---
# <a name="mft_support_3dvideo-attribute"></a>Таблица MFT \_ поддерживает \_ атрибут 3DVIDEO

Указывает, поддерживает ли Media Foundationное преобразование (MFT) трехмерное видео стереоскопик.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="remarks"></a>Комментарии

Чтобы запросить этот атрибут, вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище атрибутов MFT. Если методы **InAttribute** выполнены, вызовите [**ИМФАТТРИБУТЕС:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Значение этого атрибута по умолчанию равно **false**. Рассматривайте этот атрибут как доступный только для чтения. Не изменяйте значение. в MFT все изменения в значении будут игнорироваться.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




