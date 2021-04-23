---
title: Лицензирование
description: Лицензирование
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794023"
---
# <a name="licensing"></a><span data-ttu-id="1147b-103">Лицензирование</span><span class="sxs-lookup"><span data-stu-id="1147b-103">Licensing</span></span>

<span data-ttu-id="1147b-104">Для успешного внедрения лицензированных элементов управления контейнеры элементов управления ActiveX должны использовать [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) вместо [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="1147b-104">In order to embed licensed controls successfully, ActiveX control containers must use [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) instead of [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="1147b-105">Некоторые вспомогательные функции создания и загрузки OLE ([**олелоад**](/windows/desktop/api/Ole2/nf-ole2-oleload) и [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) явно вызывают **IClassFactory** , а не **IClassFactory2**, и поэтому не могут использоваться для создания или загрузки лицензированных элементов управления ActiveX.</span><span class="sxs-lookup"><span data-stu-id="1147b-105">Several OLE creation and loading helper functions ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) explicitly call **IClassFactory** and not **IClassFactory2**, and therefore cannot be used to create or load licensed ActiveX controls.</span></span> <span data-ttu-id="1147b-106">Контейнеры элементов управления ActiveX должны явно создавать и загружать элементы управления ActiveX с помощью **IClassFactory2**.</span><span class="sxs-lookup"><span data-stu-id="1147b-106">ActiveX control containers should explicitly create and load ActiveX Controls using **IClassFactory2**.</span></span>

 

 