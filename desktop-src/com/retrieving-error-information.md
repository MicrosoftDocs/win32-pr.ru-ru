---
title: Получение информации об ошибке
description: Получение информации об ошибке
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070651"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="1e1dc-103">Получение информации об ошибке</span><span class="sxs-lookup"><span data-stu-id="1e1dc-103">Retrieving Error Information</span></span>

<span data-ttu-id="1e1dc-104">Используя интерфейсы и функции обработки ошибок COM, можно получить сведения об ошибке следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1e1dc-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="1e1dc-105">Проверьте, представляет ли возвращаемое значение ошибку, которую объект готов к обработке.</span><span class="sxs-lookup"><span data-stu-id="1e1dc-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="1e1dc-106">Вызовите [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , чтобы получить указатель на интерфейс [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="1e1dc-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="1e1dc-107">Затем вызовите метод [**ISupportErrorInfo:: интерфацесуппортсерроринфо**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) , чтобы убедиться, что ошибка была вызвана объектом, который его вернул, а объект Error относится к текущей ошибке, а не к предыдущему вызову.</span><span class="sxs-lookup"><span data-stu-id="1e1dc-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="1e1dc-108">Чтобы получить указатель на объект Error, вызовите функцию [**жетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="1e1dc-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="1e1dc-109">Чтобы получить сведения из объекта Error, используйте методы [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="1e1dc-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="1e1dc-110">Если объект не готов к обработке ошибки, но ему необходимо распространить сведения об ошибке дальше по цепочке вызовов, он должен просто передать возвращаемое значение вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="1e1dc-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="1e1dc-111">Поскольку функция [**жетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) удаляет сведения об ошибке и передает владение объекту-ошибке вызывающему объекту, функция должна вызываться только объектом, обрабатывающим ошибку.</span><span class="sxs-lookup"><span data-stu-id="1e1dc-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 