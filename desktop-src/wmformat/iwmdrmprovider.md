---
title: Интерфейс Ивмдрмпровидер
description: Интерфейс Ивмдрмпровидер предоставляет метод, который создает другие объекты расширенных API-интерфейсов клиента DRM Microsoft Windows Media. Вы можете получить указатель на экземпляр этого интерфейса, вызвав функцию Вмдрмкреатепровидер.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Формат Windows Media в интерфейсе Ивмдрмпровидер
- Ивмдрмпровидер интерфейса Windows Media Format, описание
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793062"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="c6846-105">Интерфейс Ивмдрмпровидер</span><span class="sxs-lookup"><span data-stu-id="c6846-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="c6846-106">Интерфейс **ивмдрмпровидер** предоставляет метод, который создает другие объекты расширенных API-интерфейсов клиента DRM Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c6846-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="c6846-107">Указатель на экземпляр этого интерфейса можно получить, вызвав функцию [**вмдрмкреатепровидер**](wmdrmcreateprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="c6846-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="c6846-108">Чтобы получить указатель на экземпляр этого интерфейса, который может создавать защищенные объекты, необходимо вызвать функцию [**вмдрмкреатепротектедпровидер**](wmdrmcreateprotectedprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="c6846-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="c6846-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="c6846-109">Members</span></span>

<span data-ttu-id="c6846-110">Интерфейс **ивмдрмпровидер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c6846-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c6846-111">**Ивмдрмпровидер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c6846-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="c6846-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c6846-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6846-113">Методы</span><span class="sxs-lookup"><span data-stu-id="c6846-113">Methods</span></span>

<span data-ttu-id="c6846-114">Интерфейс **ивмдрмпровидер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c6846-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="c6846-115">Метод</span><span class="sxs-lookup"><span data-stu-id="c6846-115">Method</span></span>                                              | <span data-ttu-id="c6846-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c6846-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6846-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="c6846-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="c6846-118">Извлекает указатель на указанный интерфейс, создавая реализующий объект при необходимости.</span><span class="sxs-lookup"><span data-stu-id="c6846-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c6846-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6846-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6846-120">**Интерфейсы**</span><span class="sxs-lookup"><span data-stu-id="c6846-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

