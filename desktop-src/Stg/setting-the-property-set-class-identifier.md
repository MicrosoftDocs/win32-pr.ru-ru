---
title: Установка идентификатора класса набора свойств
description: Метод Ипропертистораже Сеткласс задает идентификатор CLSID объекта хранилища и значение тега класса, хранящееся в наборе свойств COM. Это происходит при вызове непростого хранилища свойств, хранящегося в структурированном объекте хранилища.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Установка идентификатора класса набора свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068415"
---
# <a name="setting-the-property-set-class-identifier"></a><span data-ttu-id="14989-105">Установка идентификатора класса набора свойств</span><span class="sxs-lookup"><span data-stu-id="14989-105">Setting the Property Set Class Identifier</span></span>

<span data-ttu-id="14989-106">Метод [**ипропертистораже:: сеткласс**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) задает идентификатор CLSID объекта хранилища и значение тега класса, хранящееся в наборе свойств COM.</span><span class="sxs-lookup"><span data-stu-id="14989-106">The [**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) method sets both the CLSID of the storage object and the class tag value stored in the COM property set.</span></span> <span data-ttu-id="14989-107">Это происходит при вызове непростого хранилища свойств, хранящегося в структурированном объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="14989-107">This occurs when invoked on a nonsimple property storage stored in a structured storage object.</span></span>

<span data-ttu-id="14989-108">Это обеспечивает согласованность и единообразие, что создает более эффективное взаимодействие с некоторыми инструментами.</span><span class="sxs-lookup"><span data-stu-id="14989-108">This provides consistency and uniformity which creates better interaction with some tools.</span></span> <span data-ttu-id="14989-109">Объект хранилища свойств непрост, если он создается путем вызова [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) с установленным флагом **пропсетфлаг \_ unsimple** .</span><span class="sxs-lookup"><span data-stu-id="14989-109">A property storage object is nonsimple if it is created by calling [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) with the **PROPSETFLAG\_NONSIMPLE** flag set.</span></span>

<span data-ttu-id="14989-110">Идентификатор CLSID объекта хранилища задается вызовом метода [**IStorage:: сеткласс**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span><span class="sxs-lookup"><span data-stu-id="14989-110">The CLSID of the storage object is set with a call to [**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span></span>

 

 




