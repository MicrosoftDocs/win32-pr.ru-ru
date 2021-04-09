---
title: Структура Еафостпирнапинфо (Еафостпирапис. h)
description: Содержит сведения о защите доступа к сети (NAP) по запрашивающему сторона EAP.
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- Еафостпирнапинфо структура EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3221f40dea9e84e410a1a643bbbcdc94e9039b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071940"
---
# <a name="eaphostpeernapinfo-structure"></a><span data-ttu-id="c1e88-104">Структура Еафостпирнапинфо</span><span class="sxs-lookup"><span data-stu-id="c1e88-104">EapHostPeerNapInfo structure</span></span>

<span data-ttu-id="c1e88-105">Структура **еафостпирнапинфо** содержит сведения о защите доступа к сети (NAP) на запрашивающем сторона EAP.</span><span class="sxs-lookup"><span data-stu-id="c1e88-105">The **EapHostPeerNapInfo** structure contains the Network Access Protection (NAP) information on an EAP supplicant.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1e88-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1e88-106">Syntax</span></span>


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a><span data-ttu-id="c1e88-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c1e88-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1e88-108">**исолатионстате**</span><span class="sxs-lookup"><span data-stu-id="c1e88-108">**isolationState**</span></span>
</dt> <dd>

<span data-ttu-id="c1e88-109">Структура [**\_ состояния изоляции**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) , указывающая состояние изоляции NAP компьютера.</span><span class="sxs-lookup"><span data-stu-id="c1e88-109">An [**ISOLATION\_STATE**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) structure that specifies the NAP isolation state of a computer.</span></span> <span data-ttu-id="c1e88-110">Состояние изоляции определяет уровень предоставляемого доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="c1e88-110">The isolation state determines the level of network access granted.</span></span>

</dd> <dt>

<span data-ttu-id="c1e88-111">**пробатионтиме**</span><span class="sxs-lookup"><span data-stu-id="c1e88-111">**probationTime**</span></span>
</dt> <dd>

<span data-ttu-id="c1e88-112">Структура **пробатионтиме** , указывающая время, необходимое для выхода из карантина, после которого соединение будет удалено.</span><span class="sxs-lookup"><span data-stu-id="c1e88-112">A **ProbationTime** structure that specifies the time required for the connection to come out of quarantine after which the connection will be dropped.</span></span> <span data-ttu-id="c1e88-113">Структура **пробатионтиме** идентична структуре [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="c1e88-113">A **ProbationTime** structure is identical to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c1e88-114">**стрингкоррелатионидленгс**</span><span class="sxs-lookup"><span data-stu-id="c1e88-114">**stringCorrelationIdLength**</span></span>
</dt> <dd>

<span data-ttu-id="c1e88-115">Длина [СТРИНГКОРРЕЛАТИОНИД](/windows/desktop/NAP/nap-datatypes) NAP в байтах, которая соответствует этой структуре.</span><span class="sxs-lookup"><span data-stu-id="c1e88-115">The length, in bytes, of the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) that follows this structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1e88-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1e88-116">Remarks</span></span>

<span data-ttu-id="c1e88-117">Структура **еафостпирнапинфо** предшествует [стрингкоррелатионид](/windows/desktop/NAP/nap-datatypes) NAP типа данных **WCHAR** в потоке байтов RPC.</span><span class="sxs-lookup"><span data-stu-id="c1e88-117">The **EapHostPeerNapInfo** structure precedes the NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) of data type **WCHAR** in the RPC byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e88-118">Требования</span><span class="sxs-lookup"><span data-stu-id="c1e88-118">Requirements</span></span>



| <span data-ttu-id="c1e88-119">Требование</span><span class="sxs-lookup"><span data-stu-id="c1e88-119">Requirement</span></span> | <span data-ttu-id="c1e88-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c1e88-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e88-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1e88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e88-122">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1e88-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c1e88-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1e88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e88-124">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c1e88-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c1e88-125">Header</span><span class="sxs-lookup"><span data-stu-id="c1e88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1e88-126"><dt>Еафостпирапис. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1e88-126"><dt>Eaphostpeerapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e88-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1e88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e88-128">Структуры запрашивающего сторона EAPHost</span><span class="sxs-lookup"><span data-stu-id="c1e88-128">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="c1e88-129">**еафостпиржетаусстатус**</span><span class="sxs-lookup"><span data-stu-id="c1e88-129">**EapHostPeerGetAuthStatus**</span></span>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[<span data-ttu-id="c1e88-130">**еафостпирмесодауспарамс**</span><span class="sxs-lookup"><span data-stu-id="c1e88-130">**EapHostPeerMethodAuthParams**</span></span>](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

