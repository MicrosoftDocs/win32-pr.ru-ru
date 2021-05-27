---
title: Интерфейсы хранилища
description: Интерфейсы хранилища
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549269"
---
# <a name="storage-interfaces"></a><span data-ttu-id="f5dec-103">Интерфейсы хранилища</span><span class="sxs-lookup"><span data-stu-id="f5dec-103">Storage Interfaces</span></span>

<span data-ttu-id="f5dec-104">Контейнеры элементов управления должны поддерживать элементы управления, реализующие [**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)или [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="f5dec-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="f5dec-105">При необходимости контейнер может поддерживать любые другие интерфейсы сохраняемости, такие как [**иперсистмемори**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)и [**иперсистмоникер**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , для этих элементов управления, которые обеспечивают поддержку.</span><span class="sxs-lookup"><span data-stu-id="f5dec-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="f5dec-106">После того как контейнер элементов управления ActiveX выбрал и инициализировал интерфейс хранения для использования ([**иперсистстораже**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**иперсистстреаминит**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)и т. д.), этот интерфейс хранилища останется основным интерфейсом хранилища для жизненного цикла элемента управления, т. е. Этот элемент управления останется в хранилище.</span><span class="sxs-lookup"><span data-stu-id="f5dec-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="f5dec-107">Это не исключает сохранение контейнера в других интерфейсах хранилища.</span><span class="sxs-lookup"><span data-stu-id="f5dec-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="f5dec-108">Контейнерам элементов управления ActiveX не требуется поддерживать механизм "Сохранить как текст", поэтому использование [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) и связанного с ним интерфейса [**ипропертибаг**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="f5dec-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) and the associated container-side interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5dec-109">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f5dec-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5dec-110">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="f5dec-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 