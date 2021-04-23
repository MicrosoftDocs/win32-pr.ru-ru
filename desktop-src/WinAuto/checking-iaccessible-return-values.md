---
title: Проверка возвращаемых значений IAccessible
description: Разработчикам клиентов не следует полагаться на то, что макросы модели COM были УСПЕШНЫМи и не прошли проверку возвращаемых значений IAccessible, так как значения, отличные от S \_ ОК, считаются успешными.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105710323"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="e8719-103">Проверка возвращаемых значений IAccessible</span><span class="sxs-lookup"><span data-stu-id="e8719-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="e8719-104">Разработчикам клиентов не следует полагаться на то, что макросы модели COM были [**успешными**](/windows/desktop/api/winerror/nf-winerror-succeeded) и [**не прошли**](/windows/desktop/api/winerror/nf-winerror-failed) проверку возвращаемых значений [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , так как значения, отличные от S \_ ОК, считаются успешными.</span><span class="sxs-lookup"><span data-stu-id="e8719-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="e8719-105">Например, метод может возвращать \_ значение false, которое считается успешным при **успешном** выполнении макроса, но по-прежнему получил указатель **null** в выходном параметре.</span><span class="sxs-lookup"><span data-stu-id="e8719-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="e8719-106">Разработчики клиентов должны защищаться от вероятности возврата некоторыми серверами кодов ошибок, отличных от задокументированных значений.</span><span class="sxs-lookup"><span data-stu-id="e8719-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="e8719-107">Для обеспечения безопасности необходимо убедиться, что все выходные параметры содержат действительные сведения и удовлетворяют следующим критериям.</span><span class="sxs-lookup"><span data-stu-id="e8719-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="e8719-108">Все указатели не **равны NULL**.</span><span class="sxs-lookup"><span data-stu-id="e8719-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="e8719-109">Элемент **VT** любой структуры [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) не равен VT \_ Empty.</span><span class="sxs-lookup"><span data-stu-id="e8719-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 