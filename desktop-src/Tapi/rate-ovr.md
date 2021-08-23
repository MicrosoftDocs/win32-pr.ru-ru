---
description: Скорость или пропускная способность вызова указывает скорость передачи данных. Три точки данных определяют скорость текущего значения максимальной скорости для указанного режима носителя и минимальное значение скорости для режима носителя.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Тариф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce0af0b2dd6dfe34759753f52773bafe0bdf2bf8f4472ed863dcc6c8b0f10a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060562"
---
# <a name="rate"></a>Тариф

Скорость (или пропускная способность) вызова указывает скорость передачи данных. Три точки данных определяют скорость: Текущая скорость, максимальная скорость для указанного режима носителя и минимальная скорость для режима носителя.

Не все поставщики служб поддерживают использование этих сведений.

* * TAPI 2. x: * *[**линесеткаллпарамс**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двминрате** или **двмаксрате** член [**линекаллинфо**](/windows/win32/api/tapi/ns-tapi-linecallinfo)

* * TAPI 3. x: * *[**иткаллинфо:: Get \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**иткаллинфо::p UT \_ каллинфолонг**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ максрате**, **CIL \_ минрате** или **CIL в \_** [**каллинфо \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)

* * ТСПИ: * *[**строка \_ каллинфо**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) сообщение, а для *DWPARAM1* задано \_ значение линекаллинфостате

 

 
