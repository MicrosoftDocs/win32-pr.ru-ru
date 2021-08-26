---
description: Указывает, может ли обработчик потока байтов использовать поток байтов, Открытый для записи другим потоком.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Атрибут MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ea9b6cf1d126fca44066e7d3292227ecf0ce01f3419b377b6d66b67845f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941034"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ битестреамхандлер \_ принимает \_ \_ атрибут общей записи

Указывает, может ли обработчик потока байтов использовать поток байтов, Открытый для записи другим потоком.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Обработчики потока байтов могут поддерживать этот атрибут. Чтобы получить или задать атрибут, сначала запросите обработчик потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Затем вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) или [**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Если этот атрибут имеет **значение true**, это означает, что обработчик потока байтов может считывать данные из потока, в то время как другой поток выполняет запись в тот же поток. Когда поток открывается для записи другим потоком, метод [**имфбитестреам:: Capabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) Возвращает флаг **\_ \_ записи мфбитестреам Share** .

Этот атрибут влияет на разрешение исходного кода. Если для потока байтов установлен флаг **\_ \_ записи общего ресурса мфбитестреам** , то [сопоставитель источника](source-resolver.md) не передаст поток в обработчик потока байтов, если только обработчик не имеет атрибут MF битестреамхандлер, \_ \_ принимающий \_ общий доступ \_ для записи. 

Флаг **\_ \_ записи общего ресурса мфбитестреам** является указанием того, что длина потока может измениться во время чтения обработчика из него.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                     |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Обработчики схем и обработчики Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




