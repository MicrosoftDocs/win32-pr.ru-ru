---
description: 'Версия метода Имфконтентпротектионманажер:: Бегиненаблеконтент, поддерживающая удаленное взаимодействие.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: Ремотебегиненаблеконтент (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647223"
---
# <a name="remotebeginenablecontent"></a><span data-ttu-id="3740d-103">ремотебегиненаблеконтент</span><span class="sxs-lookup"><span data-stu-id="3740d-103">RemoteBeginEnableContent</span></span>

<span data-ttu-id="3740d-104">Версия метода [**имфконтентпротектионманажер:: бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="3740d-104">Remotable version of the [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="3740d-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3740d-105">Remarks</span></span>

<span data-ttu-id="3740d-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="3740d-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3740d-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3740d-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3740d-108">Если [**бегиненаблеконтент**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="3740d-108">If [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3740d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="3740d-109">Requirements</span></span>



| <span data-ttu-id="3740d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="3740d-110">Requirement</span></span> | <span data-ttu-id="3740d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="3740d-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3740d-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3740d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3740d-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3740d-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3740d-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3740d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3740d-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3740d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3740d-116">Header</span><span class="sxs-lookup"><span data-stu-id="3740d-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3740d-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3740d-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3740d-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3740d-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3740d-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3740d-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3740d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3740d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3740d-121">**имфконтентпротектионманажер**</span><span class="sxs-lookup"><span data-stu-id="3740d-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




