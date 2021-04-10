---
title: Тфедиткукие (Мсктф. h)
description: Тип данных Тфедиткукие определяет сеанс изменения, который имеет блокировку.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- тфедиткукие
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071076"
---
# <a name="tfeditcookie"></a><span data-ttu-id="0d1dc-104">тфедиткукие</span><span class="sxs-lookup"><span data-stu-id="0d1dc-104">TfEditCookie</span></span>

<span data-ttu-id="0d1dc-105">Тип данных **тфедиткукие** определяет сеанс изменения, который имеет блокировку.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="0d1dc-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d1dc-106">Remarks</span></span>

<span data-ttu-id="0d1dc-107">Тип данных **тфедиткукие** предоставляется диспетчером TSF и используется клиентом (приложением или службой текстового ввода) для обнаружения сеанса изменения с блокировкой только для чтения или для чтения и записи в различных методах.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="0d1dc-108">Значение **тфедиткукие** получается одним из следующих способов.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="0d1dc-109">Клиент вызывает [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="0d1dc-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="0d1dc-110">Диспетчер TSF вызывает метод Client [итфедитсессион::D оедитсессион](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .</span><span class="sxs-lookup"><span data-stu-id="0d1dc-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="0d1dc-111">Диспетчер TSF вызывает метод [итфкомпоситионсинк:: онкомпоситионтерминатед](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) клиента.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="0d1dc-112">Диспетчер TSF вызывает метод [итфклеанупконтекстсинк:: онклеанупконтекст](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) клиента.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="0d1dc-113">Диспетчер TSF вызывает метод [итфтекстедитсинк:: онендедит](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) клиента.</span><span class="sxs-lookup"><span data-stu-id="0d1dc-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d1dc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0d1dc-114">Requirements</span></span>



| <span data-ttu-id="0d1dc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0d1dc-115">Requirement</span></span> | <span data-ttu-id="0d1dc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0d1dc-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0d1dc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d1dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d1dc-118">Приложения Windows 2000 Professional \[ классические приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0d1dc-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="0d1dc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d1dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d1dc-120">\[Приложения UWP для классических приложений Windows 2000 \|\]</span><span class="sxs-lookup"><span data-stu-id="0d1dc-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="0d1dc-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0d1dc-121">Redistributable</span></span><br/>          | <span data-ttu-id="0d1dc-122">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="0d1dc-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="0d1dc-123">Header</span><span class="sxs-lookup"><span data-stu-id="0d1dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d1dc-124"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d1dc-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d1dc-125">IDL</span><span class="sxs-lookup"><span data-stu-id="0d1dc-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d1dc-126"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d1dc-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d1dc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d1dc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1dc-128">**Итфклеанупконтекстсинк:: Онклеанупконтекст**</span><span class="sxs-lookup"><span data-stu-id="0d1dc-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="0d1dc-129">**Итфкомпоситионсинк:: Онкомпоситионтерминатед**</span><span class="sxs-lookup"><span data-stu-id="0d1dc-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="0d1dc-130">**ITfDocumentMgr:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="0d1dc-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="0d1dc-131">**Итфедитсессион::D Оедитсессион**</span><span class="sxs-lookup"><span data-stu-id="0d1dc-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="0d1dc-132">**Итфтекстедитсинк:: Онендедит**</span><span class="sxs-lookup"><span data-stu-id="0d1dc-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





