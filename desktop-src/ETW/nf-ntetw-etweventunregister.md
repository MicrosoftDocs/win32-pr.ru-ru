---
UID: NF:ntw.EtwEventUnregister
title: Функция Етвевентунрегистер
description: Отменяет регистрацию события.
old-location: ''
ms.assetid: na
ms.date: 02/20/2018
ms.keywords: EtwEventUnregister
ms.topic: reference
req.header: ntetw.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10, version 1803 [desktop apps \| UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ntetw.h
api_name:
- EtwEventUnregister
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: e61de5aa1c050aedd2c82dec471765baa7e6cdd7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104133811"
---
# <a name="etweventunregister-function"></a><span data-ttu-id="257d0-103">Функция Етвевентунрегистер</span><span class="sxs-lookup"><span data-stu-id="257d0-103">EtwEventUnregister function</span></span>


## <a name="description"></a><span data-ttu-id="257d0-104">Описание</span><span class="sxs-lookup"><span data-stu-id="257d0-104">Description</span></span>


<span data-ttu-id="257d0-105"><b>Етвевентунрегистер</b> отменяет регистрацию события.</span><span class="sxs-lookup"><span data-stu-id="257d0-105">The <b>EtwEventUnregister</b> unregisters an event.</span></span>
            

<span data-ttu-id="257d0-106">Поставщики могут вызывать эту функцию только из своей функции <a href="/windows/desktop/ETW/controlcallback">контролкаллбакк</a> .</span><span class="sxs-lookup"><span data-stu-id="257d0-106">Providers can only call this function from their <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> function.</span></span>


## <a name="parameters"></a><span data-ttu-id="257d0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="257d0-107">Parameters</span></span>




### <a name="reghandle-in"></a><span data-ttu-id="257d0-108">Регхандле [in]</span><span class="sxs-lookup"><span data-stu-id="257d0-108">RegHandle [in]</span></span>

<span data-ttu-id="257d0-109">Дескриптор события.</span><span class="sxs-lookup"><span data-stu-id="257d0-109">Handle to an event.</span></span>


## <a name="returns"></a><span data-ttu-id="257d0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="257d0-110">Returns</span></span>



<span data-ttu-id="257d0-111">Возвращает значение HRESULT.</span><span class="sxs-lookup"><span data-stu-id="257d0-111">Returns an HRESULT.</span></span>





## <a name="remarks"></a><span data-ttu-id="257d0-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="257d0-112">Remarks</span></span>



## <a name="see-also"></a><span data-ttu-id="257d0-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="257d0-113">See also</span></span>