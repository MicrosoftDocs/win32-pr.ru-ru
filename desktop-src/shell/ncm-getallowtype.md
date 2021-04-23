---
description: Извлекает типы сетевых адресов, принимаемые указанным элементом управления сетью.
title: Сообщение NCM_GETALLOWTYPE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1B06463F-0CA6-4e8e-BD3B-917562A6A244
api_name:
- NCM_GETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d93cb3cff575c18764e352da54a717d7c557001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080373"
---
# <a name="ncm_getallowtype-message"></a><span data-ttu-id="5386a-103">\_Сообщение НКМ жеталловтипе</span><span class="sxs-lookup"><span data-stu-id="5386a-103">NCM\_GETALLOWTYPE message</span></span>

<span data-ttu-id="5386a-104">Извлекает типы сетевых адресов, принимаемые указанным элементом управления сетью.</span><span class="sxs-lookup"><span data-stu-id="5386a-104">Retrieves the network address types that a specified network address control accepts.</span></span>


```C++
NCM_GETALLOWTYPE

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="5386a-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="5386a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5386a-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5386a-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5386a-107">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5386a-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5386a-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5386a-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5386a-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="5386a-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5386a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5386a-110">Return value</span></span>

<span data-ttu-id="5386a-111">Возвращает разрешенные типы сетевых адресов в виде одной или нескольких констант типа "сеть — [**\_ строка**](net-string.md) ".</span><span class="sxs-lookup"><span data-stu-id="5386a-111">Returns the allowed network address types as one or more of the [**NET\_STRING**](net-string.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="5386a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="5386a-112">Remarks</span></span>

<span data-ttu-id="5386a-113">Возвращенная маска — это критерий, используемый для проверки сетевого адреса в сообщении [**НКМ- \_ Address**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="5386a-113">The returned mask is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="5386a-114">Это сообщение используется только для управления сетевыми адресами.</span><span class="sxs-lookup"><span data-stu-id="5386a-114">Use this message for a network address control only.</span></span> <span data-ttu-id="5386a-115">Чтобы создать экземпляр, используйте класс **мсктлс \_ нетаддресс** , определенный в шеллапи. h.</span><span class="sxs-lookup"><span data-stu-id="5386a-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="5386a-116">Вызовите [**инитнетворкаддрессконтрол**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) во время выполнения перед отправкой этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="5386a-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="5386a-117">Будет инициализирована библиотека общих элементов управления, содержащая элемент управления "сетевой адрес".</span><span class="sxs-lookup"><span data-stu-id="5386a-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5386a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="5386a-118">Requirements</span></span>



| <span data-ttu-id="5386a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="5386a-119">Requirement</span></span> | <span data-ttu-id="5386a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="5386a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5386a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5386a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5386a-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5386a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5386a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5386a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5386a-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5386a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5386a-125">Header</span><span class="sxs-lookup"><span data-stu-id="5386a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5386a-126"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="5386a-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5386a-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5386a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5386a-128">**НКМ \_ сеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="5386a-128">**NCM\_SETALLOWTYPE**</span></span>](ncm-setallowtype.md)
</dt> <dt>

[<span data-ttu-id="5386a-129">**Нетаддр \_ жеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="5386a-129">**NetAddr\_GetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getallowtype)
</dt> </dl>

 

 




