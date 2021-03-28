---
description: Задает типы сетевых адресов, принимаемые указанным элементом управления для сетевых адресов.
title: Сообщение NCM_SETALLOWTYPE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FD998452-047A-4aea-A08E-8F6F8C30115B
api_name:
- NCM_SETALLOWTYPE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d9cc822e07022a01439fbe7e41243bd1b78e636b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810942"
---
# <a name="ncm_setallowtype-message"></a><span data-ttu-id="dda70-103">\_Сообщение НКМ сеталловтипе</span><span class="sxs-lookup"><span data-stu-id="dda70-103">NCM\_SETALLOWTYPE message</span></span>

<span data-ttu-id="dda70-104">Задает типы сетевых адресов, принимаемые указанным элементом управления для сетевых адресов.</span><span class="sxs-lookup"><span data-stu-id="dda70-104">Sets the network address types that a specified network address control accepts.</span></span>


```C++
NCM_SETALLOWTYPE

    wParam = (WPARAM) (DWORD) addrMask;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="dda70-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="dda70-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dda70-106">*аддрмаск* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dda70-106">*addrMask* \[in\]</span></span>
</dt> <dd><span data-ttu-id="dda70-107">Указывает типы сетевых адресов в виде одной или нескольких констант типа "сеть — <a href="net-string.md">**\_ строка**</a> ".</span><span class="sxs-lookup"><span data-stu-id="dda70-107">Specifies the network address types as one or more of the <a href="net-string.md">**NET\_STRING**</a> constants.</span></span></dd> <dt>

<span data-ttu-id="dda70-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dda70-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dda70-109">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="dda70-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dda70-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dda70-110">Return value</span></span>

<span data-ttu-id="dda70-111">Возвращает \_ значение ОК, если успешно, или в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dda70-111">Returns S\_OK if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda70-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="dda70-112">Remarks</span></span>

<span data-ttu-id="dda70-113">Набор масок — это критерий, используемый для проверки сетевого адреса в сообщении [**НКМ- \_ Address**](ncm-getaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="dda70-113">The mask set is the criterion used to validate a network address in the [**NCM\_GETADDRESS**](ncm-getaddress.md) message.</span></span>

<span data-ttu-id="dda70-114">Это сообщение используется только для управления сетевыми адресами.</span><span class="sxs-lookup"><span data-stu-id="dda70-114">Use this message for a network address control only.</span></span> <span data-ttu-id="dda70-115">Чтобы создать экземпляр, используйте класс **мсктлс \_ нетаддресс** , определенный в шеллапи. h.</span><span class="sxs-lookup"><span data-stu-id="dda70-115">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="dda70-116">Вызовите [**инитнетворкаддрессконтрол**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) во время выполнения перед отправкой этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="dda70-116">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="dda70-117">Будет инициализирована библиотека общих элементов управления, содержащая элемент управления "сетевой адрес".</span><span class="sxs-lookup"><span data-stu-id="dda70-117">This initializes the common controls library that contains the network address control.</span></span>

## <a name="requirements"></a><span data-ttu-id="dda70-118">Требования</span><span class="sxs-lookup"><span data-stu-id="dda70-118">Requirements</span></span>



| <span data-ttu-id="dda70-119">Требование</span><span class="sxs-lookup"><span data-stu-id="dda70-119">Requirement</span></span> | <span data-ttu-id="dda70-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dda70-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dda70-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dda70-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dda70-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dda70-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dda70-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dda70-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dda70-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dda70-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dda70-125">Header</span><span class="sxs-lookup"><span data-stu-id="dda70-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dda70-126"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="dda70-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dda70-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dda70-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dda70-128">**НКМ \_ жеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="dda70-128">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="dda70-129">**Нетаддр \_ сеталловтипе**</span><span class="sxs-lookup"><span data-stu-id="dda70-129">**NetAddr\_SetAllowType**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype)
</dt> </dl>

 

 




