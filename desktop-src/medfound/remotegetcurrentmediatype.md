---
description: 'Версия метода Имфмедиатипехандлер:: Жеткуррентмедиатипе, поддерживающая удаленное взаимодействие.'
ms.assetid: f7f69adb-2a4a-47a9-bb92-ad9d005b962f
title: Ремотежеткуррентмедиатипе (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc168198e8402d83538c046967d1d851ae2532b1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703433"
---
# <a name="remotegetcurrentmediatype"></a><span data-ttu-id="79b38-103">ремотежеткуррентмедиатипе</span><span class="sxs-lookup"><span data-stu-id="79b38-103">RemoteGetCurrentMediaType</span></span>

<span data-ttu-id="79b38-104">Версия метода [**имфмедиатипехандлер:: жеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="79b38-104">Remotable version of the [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) method.</span></span>

``` syntax
[call_as(GetCurrentMediaType)]
HRESULT RemoteGetCurrentMediaType(
    BYTE **ppbData,
    DWORD *pcbData
);
```

## <a name="remarks"></a><span data-ttu-id="79b38-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79b38-105">Remarks</span></span>

<span data-ttu-id="79b38-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="79b38-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="79b38-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="79b38-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="79b38-108">Если [**жеткуррентмедиатипе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="79b38-108">If [**GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

<span data-ttu-id="79b38-109">Этот интерфейс доступен на следующих платформах, если установлены распространяемые компоненты пакета SDK Windows Media Format 11.</span><span class="sxs-lookup"><span data-stu-id="79b38-109">This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:</span></span>

-   <span data-ttu-id="79b38-110">Windows XP с пакетом обновления 2 (SP2) и более поздние версии.</span><span class="sxs-lookup"><span data-stu-id="79b38-110">Windows XP with Service Pack 2 (SP2) and later.</span></span>
-   <span data-ttu-id="79b38-111">Windows XP Media Center Edition 2005 с KB900325 (Windows XP Media Center Edition 2005) и KB925766 (Октябрь 2006 накопительный пакет обновления для Windows XP Media Center Edition).</span><span class="sxs-lookup"><span data-stu-id="79b38-111">Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="79b38-112">Требования</span><span class="sxs-lookup"><span data-stu-id="79b38-112">Requirements</span></span>



| <span data-ttu-id="79b38-113">Требование</span><span class="sxs-lookup"><span data-stu-id="79b38-113">Requirement</span></span> | <span data-ttu-id="79b38-114">Значение</span><span class="sxs-lookup"><span data-stu-id="79b38-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79b38-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79b38-115">Minimum supported client</span></span><br/> | <span data-ttu-id="79b38-116">\[Приложения UWP для классических приложений Windows Vista \|\]</span><span class="sxs-lookup"><span data-stu-id="79b38-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="79b38-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79b38-117">Minimum supported server</span></span><br/> | <span data-ttu-id="79b38-118">\[Приложения UWP для классических приложений Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="79b38-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="79b38-119">Header</span><span class="sxs-lookup"><span data-stu-id="79b38-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="79b38-120"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79b38-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="79b38-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79b38-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="79b38-122"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79b38-122"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="79b38-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79b38-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b38-124">**имфмедиатипехандлер**</span><span class="sxs-lookup"><span data-stu-id="79b38-124">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
</dt> </dl>

 

 




