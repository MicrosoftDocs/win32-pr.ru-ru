---
description: 'Версия метода Имфпмфост:: Креатеобжектбиклсид, поддерживающая удаленное взаимодействие.'
ms.assetid: be96be6d-47de-4d2b-81fc-13079de33888
title: Ремотекреатеобжектбиклсид (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e57307ece851484675d01a699037647efad771d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662615"
---
# <a name="remotecreateobjectbyclsid"></a><span data-ttu-id="fa197-103">ремотекреатеобжектбиклсид</span><span class="sxs-lookup"><span data-stu-id="fa197-103">RemoteCreateObjectByCLSID</span></span>

<span data-ttu-id="fa197-104">Версия метода [**имфпмфост:: креатеобжектбиклсид**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) , поддерживающая удаленное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="fa197-104">Remotable version of the [**IMFPMPHost::CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) method.</span></span>

``` syntax
[call_as(CreateObjectByCLSID)]
HRESULT RemoteCreateObjectByCLSID( 
    REFCLSID clsid,
    BYTE *pbData, 
    DWORD cbData, 
    REFIID riid,
    void **ppv
);
```

## <a name="remarks"></a><span data-ttu-id="fa197-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fa197-105">Remarks</span></span>

<span data-ttu-id="fa197-106">Приложения не могут вызывать этот метод напрямую, и объекты не реализуют этот метод.</span><span class="sxs-lookup"><span data-stu-id="fa197-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="fa197-107">Метод не отображается в таблице vtable для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fa197-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="fa197-108">Если [**креатеобжектбиклсид**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) вызывается через границы процесса, то библиотека DLL прокси или заглушки Media Foundation преобразует вызов в вызов удаленного метода и затем преобразует его обратно.</span><span class="sxs-lookup"><span data-stu-id="fa197-108">If [**CreateObjectByCLSID**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa197-109">Требования</span><span class="sxs-lookup"><span data-stu-id="fa197-109">Requirements</span></span>



| <span data-ttu-id="fa197-110">Требование</span><span class="sxs-lookup"><span data-stu-id="fa197-110">Requirement</span></span> | <span data-ttu-id="fa197-111">Значение</span><span class="sxs-lookup"><span data-stu-id="fa197-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa197-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa197-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fa197-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fa197-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fa197-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa197-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fa197-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fa197-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fa197-116">Header</span><span class="sxs-lookup"><span data-stu-id="fa197-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa197-117"><dt>Мфобжектс. h (включение Мфидл. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fa197-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="fa197-118">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fa197-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa197-119"><dt>Мфууид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa197-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="fa197-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa197-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa197-121">**имфпмфост**</span><span class="sxs-lookup"><span data-stu-id="fa197-121">**IMFPMPHost**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost)
</dt> <dt>

[<span data-ttu-id="fa197-122">Сеанс PMP мультимедиа</span><span class="sxs-lookup"><span data-stu-id="fa197-122">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="fa197-123">Путь к защищенному носителю</span><span class="sxs-lookup"><span data-stu-id="fa197-123">Protected Media Path</span></span>](protected-media-path.md)
</dt> </dl>

 

 




