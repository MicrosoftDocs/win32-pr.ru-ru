---
description: Отображает сообщение об ошибке в всплывающей подсказке, связанной с элементом управления "сетевой адрес".
title: Сообщение NCM_DISPLAYERRORTIP (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997255"
---
# <a name="ncm_displayerrortip-message"></a><span data-ttu-id="cc9b5-103">\_Сообщение НКМ дисплайеррортип</span><span class="sxs-lookup"><span data-stu-id="cc9b5-103">NCM\_DISPLAYERRORTIP message</span></span>

<span data-ttu-id="cc9b5-104">Отображает сообщение об ошибке в всплывающей подсказке, связанной с элементом управления "сетевой адрес".</span><span class="sxs-lookup"><span data-stu-id="cc9b5-104">Displays an error message in the balloon tip associated with the network address control.</span></span>


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="cc9b5-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc9b5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc9b5-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc9b5-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cc9b5-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cc9b5-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc9b5-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cc9b5-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc9b5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc9b5-110">Return value</span></span>

<span data-ttu-id="cc9b5-111">Если это сообщение завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="cc9b5-111">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc9b5-112">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc9b5-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc9b5-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="cc9b5-113">Remarks</span></span>

<span data-ttu-id="cc9b5-114">Отправка этого сообщения для вывода сообщения об ошибке, когда адрес, введенный в элементе управления, не проверяется по разрешенным типам сетевых адресов, заданным с помощью сообщения [**НКМ \_ сеталловтипе**](ncm-setallowtype.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9b5-114">Send this message to display an error message when an address typed into the control does not validate against the allowed network address types set with the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message.</span></span> <span data-ttu-id="cc9b5-115">Чтобы проверить адрес, используйте сообщение [**НКМ \_**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="cc9b5-115">Use the [**NCM\_GETADDRESS**](ncm-getaddress.md) message to validate the address.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9b5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cc9b5-116">Requirements</span></span>



| <span data-ttu-id="cc9b5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cc9b5-117">Requirement</span></span> | <span data-ttu-id="cc9b5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cc9b5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9b5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc9b5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cc9b5-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc9b5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc9b5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc9b5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cc9b5-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc9b5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc9b5-123">Header</span><span class="sxs-lookup"><span data-stu-id="cc9b5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc9b5-124"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc9b5-124"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc9b5-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc9b5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc9b5-126">**Нетаддр \_ дисплайеррортип**</span><span class="sxs-lookup"><span data-stu-id="cc9b5-126">**NetAddr\_DisplayErrorTip**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




