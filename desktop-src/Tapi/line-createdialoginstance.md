---
description: Сообщение ТСПИ LINE \_ креатедиалогинстанце заставляет TAPI создать связь между поставщиком службы и экземпляром функции туиспи провидерженерикдиалог, которая \_ выполняется в контексте приложения.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Сообщение LINE_CREATEDIALOGINSTANCE (Тспи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e670a0dbcdde82721e5441b95983d5852e821cc981062947a0d6b76639ad762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873504"
---
# <a name="line_createdialoginstance-message"></a>Строка \_ сообщения креатедиалогинстанце

Сообщение ТСПИ **Line \_ КРЕАТЕДИАЛОГИНСТАНЦЕ** заставляет TAPI создать связь между поставщиком услуг и экземпляром функции [**туиспи \_ провидерженерикдиалог**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) , которая выполняется в контексте приложения, вызвавшего асинхронную функцию Тспи, определяемую параметром *Дврекуестид* структуры [**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) , на которую указывает *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хпровидер* 
</dt> <dd>

Провидерхандле, предоставляемый поставщику услуг в качестве параметра для [**тспи \_ провидеренумдевицес**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*лптуиспикреатедиалогинстанцепарамс* 
</dt> <dd>

Указатель на структуру [**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>Тспи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ТСПИ \_ провидеренумдевицес**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**туиспикреатедиалогинстанцепарамс**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

