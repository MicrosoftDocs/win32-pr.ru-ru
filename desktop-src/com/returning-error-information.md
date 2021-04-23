---
title: Возврат сведений об ошибке
description: Возврат сведений об ошибке
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413785"
---
# <a name="returning-error-information"></a><span data-ttu-id="48163-103">Возврат сведений об ошибке</span><span class="sxs-lookup"><span data-stu-id="48163-103">Returning Error Information</span></span>

<span data-ttu-id="48163-104">Используя интерфейсы и функции обработки ошибок COM, вы можете вернуть сведения об ошибке, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="48163-104">Using the COM error-handling interfaces and functions, you can return error information by performing the following the steps:</span></span>

1.  <span data-ttu-id="48163-105">Реализуйте интерфейс [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="48163-105">Implement the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span>
2.  <span data-ttu-id="48163-106">Чтобы создать экземпляр общего объекта Error, вызовите функцию [**креатирроринфо**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="48163-106">To create an instance of the generic error object, call the [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) function.</span></span>
3.  <span data-ttu-id="48163-107">Чтобы задать его содержимое, используйте методы [**икреатирроринфо**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="48163-107">To set its contents, use the [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) methods.</span></span>
4.  <span data-ttu-id="48163-108">Чтобы связать объект Error с текущим логическим потоком, вызовите функцию [**сетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="48163-108">To associate the error object with the current logical thread, call the [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) function.</span></span>

<span data-ttu-id="48163-109">Интерфейсы обработки ошибок создают и управляют объектом Error, который предоставляет сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="48163-109">The error handling interfaces create and manage an error object, which provides information about the error.</span></span> <span data-ttu-id="48163-110">Объект ошибки не совпадает с объектом, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="48163-110">The error object is not the same as the object that encountered the error.</span></span> <span data-ttu-id="48163-111">Это отдельный объект, связанный с текущим потоком выполнения.</span><span class="sxs-lookup"><span data-stu-id="48163-111">It is a separate object associated with the current thread of execution.</span></span>

 

 