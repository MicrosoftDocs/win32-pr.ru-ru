---
title: Тфклиентид (Мсктф. h)
description: Тип данных Тфклиентид используется для обнаружения клиента.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- тфклиентид
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801805"
---
# <a name="tfclientid"></a><span data-ttu-id="bf2cf-104">тфклиентид</span><span class="sxs-lookup"><span data-stu-id="bf2cf-104">TfClientId</span></span>

<span data-ttu-id="bf2cf-105">Тип данных **тфклиентид** используется для обнаружения клиента.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="bf2cf-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf2cf-106">Remarks</span></span>

<span data-ttu-id="bf2cf-107">В TSF приложения и текстовые службы обычно называются клиентами.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="bf2cf-108">Каждый клиент получает уникальный идентификатор, который используется для идентификации при вызове различных методов диспетчера TSF.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="bf2cf-109">Этот идентификатор имеет тип **тфклиентид** .</span><span class="sxs-lookup"><span data-stu-id="bf2cf-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="bf2cf-110">Тип данных **тфклиентид** предоставляется диспетчером TSF.</span><span class="sxs-lookup"><span data-stu-id="bf2cf-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="bf2cf-111">Приложение получает значение **тфклиентид** при вызове [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="bf2cf-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="bf2cf-112">Значение Тфклиентид для службы текстового ввода передается методу [итфтекстинпутпроцессор:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="bf2cf-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="bf2cf-113">Любой объект, который не соответствует указанным выше категориям, может получить идентификатор клиента путем вызова [итфклиентид:: ClientID](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span><span class="sxs-lookup"><span data-stu-id="bf2cf-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2cf-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bf2cf-114">Requirements</span></span>



| <span data-ttu-id="bf2cf-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bf2cf-115">Requirement</span></span> | <span data-ttu-id="bf2cf-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bf2cf-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2cf-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf2cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2cf-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bf2cf-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="bf2cf-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf2cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2cf-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf2cf-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bf2cf-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="bf2cf-121">Redistributable</span></span><br/>          | <span data-ttu-id="bf2cf-122">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="bf2cf-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="bf2cf-123">Header</span><span class="sxs-lookup"><span data-stu-id="bf2cf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2cf-124"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2cf-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf2cf-125">IDL</span><span class="sxs-lookup"><span data-stu-id="bf2cf-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf2cf-126"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf2cf-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2cf-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf2cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2cf-128">**Итфклиентид:: ClientId**</span><span class="sxs-lookup"><span data-stu-id="bf2cf-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="bf2cf-129">**Итфтекстинпутпроцессор:: Activate**</span><span class="sxs-lookup"><span data-stu-id="bf2cf-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="bf2cf-130">**ITfThreadMgr:: Activate**</span><span class="sxs-lookup"><span data-stu-id="bf2cf-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





