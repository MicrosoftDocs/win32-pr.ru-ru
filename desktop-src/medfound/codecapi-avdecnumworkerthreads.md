---
description: Задает число рабочих потоков, используемых видеодекодером.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Свойство CODECAPI_AVDecNumWorkerThreads (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710844"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>КОДЕКАПИ \_ авдекнумворкерсреадс, свойство

Задает число рабочих потоков, используемых видеодекодером.

## <a name="data-type"></a>Тип данных

**Long** (**VT \_ I4**)

## <a name="property-guid"></a>GUID свойства

КОДЕКАПИ \_ авдекнумворкерсреадс

## <a name="remarks"></a>Комментарии

Если значение равно 1, декодер выбирает число потоков.

Для интерфейса [**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi) задайте для этого свойства значение **Long** (**VT \_ I4**). Для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) установите это свойство как **UINT32**, хотя значение подписывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**икодекапи**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

