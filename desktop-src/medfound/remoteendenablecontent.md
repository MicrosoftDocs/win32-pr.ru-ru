---
description: 'Версия метода Имфконтентпротектионманажер:: Енденаблеконтент, поддерживающая удаленное взаимодействие.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: Ремотинденаблеконтент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898182"
---
# <a name="remoteendenablecontent"></a><span data-ttu-id="162c6-103">ремотинденаблеконтент</span><span class="sxs-lookup"><span data-stu-id="162c6-103">RemoteEndEnableContent</span></span>

<span data-ttu-id="162c6-104">Версия метода [**имфконтентпротектионманажер:: енденаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="162c6-104">Remotable version of the [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) method.</span></span>

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="162c6-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="162c6-105">Remarks</span></span>

<span data-ttu-id="162c6-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="162c6-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="162c6-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="162c6-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="162c6-108">Если [**енденаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="162c6-108">If [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="162c6-109">Требования</span><span class="sxs-lookup"><span data-stu-id="162c6-109">Requirements</span></span>



| <span data-ttu-id="162c6-110">Требование</span><span class="sxs-lookup"><span data-stu-id="162c6-110">Requirement</span></span> | <span data-ttu-id="162c6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="162c6-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="162c6-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="162c6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="162c6-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="162c6-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="162c6-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="162c6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="162c6-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="162c6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="162c6-116">Header</span><span class="sxs-lookup"><span data-stu-id="162c6-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="162c6-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="162c6-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="162c6-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="162c6-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="162c6-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="162c6-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="162c6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="162c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="162c6-121">**имфконтентпротектионманажер**</span><span class="sxs-lookup"><span data-stu-id="162c6-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




