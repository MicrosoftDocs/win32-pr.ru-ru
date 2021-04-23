---
title: Повторное посещение правил агрегирования COM с помощью расширений ADSI
description: Ниже приведен краткий обзор правил агрегирования COM и расширения ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Расширения ADSI, правила объединения COM
- ADSI агрегирования COM
- Повторное посещение правил агрегирования COM с помощью расширений ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793843"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a><span data-ttu-id="b441b-106">Повторное посещение правил агрегирования COM с помощью расширений ADSI</span><span class="sxs-lookup"><span data-stu-id="b441b-106">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>

<span data-ttu-id="b441b-107">Ниже приведен краткий обзор правил агрегирования COM и расширения ADSI.</span><span class="sxs-lookup"><span data-stu-id="b441b-107">The following is a brief review of COM aggregation and ADSI extension rules.</span></span>

-   <span data-ttu-id="b441b-108">Метод **CreateInstance** возвращает указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , как показано ниже, который не делегирует вызовы функций в агрегатор.</span><span class="sxs-lookup"><span data-stu-id="b441b-108">The **CreateInstance** method returns a pointer to an [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface, as follows, that does not delegate any function calls to the aggregator.</span></span>

    <span data-ttu-id="b441b-109">Метод [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Возвращает указатели на интерфейсы, которые он поддерживает, и ошибки для интерфейсов, которые он не поддерживает.</span><span class="sxs-lookup"><span data-stu-id="b441b-109">The [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method returns pointers to the interfaces that it supports, and errors for interfaces it does not support.</span></span>

    <span data-ttu-id="b441b-110">Метод [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) увеличивает значение счетчика ссылок для объекта агрегированного расширения.</span><span class="sxs-lookup"><span data-stu-id="b441b-110">The [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) method increments the reference count on the aggregated extension object itself.</span></span>

    <span data-ttu-id="b441b-111">Метод [**иунковн:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) уменьшает значение счетчика ссылок на объекте агрегированного расширения и удаляет себя, если счетчик ссылок равен 0.</span><span class="sxs-lookup"><span data-stu-id="b441b-111">The [**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method decrements the reference count on the aggregated extension object itself and destroys itself when the reference count is 0.</span></span>

-   <span data-ttu-id="b441b-112">В объекте расширения должен храниться указатель [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) агрегатора, например m \_ паутерункновн, во время реализации метода **CreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="b441b-112">The extension object should store the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer of the aggregator, such as m\_pOuterUnknown, during the implementation of the **CreateInstance** method.</span></span>
-   <span data-ttu-id="b441b-113">Все интерфейсы, поддерживаемые объектом Extension, включая [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension), должны наследовать от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), который делегирует все вызовы функций обратно в агрегатор.</span><span class="sxs-lookup"><span data-stu-id="b441b-113">All interfaces that the extension object supports, including [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), should inherit from [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), which delegates all function calls back to the aggregator.</span></span>
    -   <span data-ttu-id="b441b-114">[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) вызывает "m \_ Паутерункновн->QueryInterface"</span><span class="sxs-lookup"><span data-stu-id="b441b-114">[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) calls "m\_pOuterUnknown->QueryInterface"</span></span>
    -   <span data-ttu-id="b441b-115">[**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) вызывает "m \_ Паутерункновн->AddRef"</span><span class="sxs-lookup"><span data-stu-id="b441b-115">[**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) calls "m\_pOuterUnknown->AddRef"</span></span>
    -   <span data-ttu-id="b441b-116">[**Иунковн:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) вызывает "m \_ Паутерункновн->Release"</span><span class="sxs-lookup"><span data-stu-id="b441b-116">[**IUnkown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) calls "m\_pOuterUnknown->Release"</span></span>

<span data-ttu-id="b441b-117">Модули записи расширений могут выбирать любую внутреннюю реализацию, если они подчиняются стандартным правилам агрегирования COM.</span><span class="sxs-lookup"><span data-stu-id="b441b-117">Extension writers can choose any internal implementation they prefer as long as they obey standard COM aggregation rules.</span></span> <span data-ttu-id="b441b-118">Имейте в виду, что объект расширения не должен работать как автономный объект.</span><span class="sxs-lookup"><span data-stu-id="b441b-118">Be aware that an extension object does not have to work as a standalone object.</span></span> <span data-ttu-id="b441b-119">Расширения предназначены для работы в виде статистических выражений.</span><span class="sxs-lookup"><span data-stu-id="b441b-119">Extensions are designed to work as aggregates.</span></span> <span data-ttu-id="b441b-120">Однако расширение может быть написано для работы как как автономный объект, так и как агрегатная функция.</span><span class="sxs-lookup"><span data-stu-id="b441b-120">However, an extension can be written to work as both a standalone object and as an aggregate.</span></span>

<span data-ttu-id="b441b-121">Помимо стандартной поддержки агрегирования COM, объект расширения может поддерживать [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension) для более сложных функций.</span><span class="sxs-lookup"><span data-stu-id="b441b-121">In addition to standard COM aggregation support, an extension object may support [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) for more advanced features.</span></span> <span data-ttu-id="b441b-122">Если поддерживается позднее связывание, расширение должно:</span><span class="sxs-lookup"><span data-stu-id="b441b-122">If late binding is supported, the extension should:</span></span>

-   <span data-ttu-id="b441b-123">Делегировать функции для [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) обратно в агрегатор.</span><span class="sxs-lookup"><span data-stu-id="b441b-123">Delegate functions for [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) back to the aggregator.</span></span>
-   <span data-ttu-id="b441b-124">Реализуйте интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) в [**иадсекстенсион**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span><span class="sxs-lookup"><span data-stu-id="b441b-124">Implement the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface in [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).</span></span>

 

 