---
description: Указывает, зарегистрировано ли преобразование Media Foundation (MFT) только в процессе приложений.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Атрибут MFT_PROCESS_LOCAL_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811608"
---
# <a name="mft_process_local_attribute-attribute"></a>\_ \_ Атрибут локального атрибута процесса MFT \_

Указывает, регистрируется ли преобразование Media Foundation (MFT) только в процессе приложения.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Этот атрибут используется следующим образом:

1.  Приложение регистрирует локальную таблицу MFT, вызывая функцию [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) или [**мфтрегистерлокалбиклсид**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) . Эти функции регистрируют MFT в процессе приложения.
2.  Функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) вызывается для перечисления МФТС, соответствующих определенному набору критериев. Приложение может напрямую вызывать функцию **мфтенумекс** , но чаще эта функция вызывается загрузчиком топологии.
3.  Функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) извлекает массив указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , каждый из которых представляет объект активации для MFT. Если таблица MFT зарегистрирована локально, \_ \_ атрибут локального атрибута процесса MFT \_ имеет значение **true** для соответствующего объекта активации.

Значение по умолчанию для этого атрибута — **false**.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




