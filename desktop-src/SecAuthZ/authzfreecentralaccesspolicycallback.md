---
description: Функция Аусзфрицентралакцессполицикаллбакк является определяемой приложением функцией, которая освобождает память, выделенную функцией Аусзжетцентралакцессполицикаллбакк.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Функция обратного вызова Аусзфрицентралакцессполицикаллбакк
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104273098"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="b04a9-103">Функция обратного вызова Аусзфрицентралакцессполицикаллбакк</span><span class="sxs-lookup"><span data-stu-id="b04a9-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="b04a9-104">Функция *аусзфрицентралакцессполицикаллбакк* является определяемой приложением функцией, которая освобождает память, выделенную функцией [*аусзжетцентралакцессполицикаллбакк*](authzgetcentralaccesspolicycallback-.md) .</span><span class="sxs-lookup"><span data-stu-id="b04a9-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="b04a9-105">*Аусзфрицентралакцессполицикаллбакк* — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="b04a9-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b04a9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b04a9-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="b04a9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b04a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04a9-108">*пцентралакцессполици* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b04a9-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b04a9-109">Указатель на политику централизованного доступа, которую необходимо освободить.</span><span class="sxs-lookup"><span data-stu-id="b04a9-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04a9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b04a9-110">Return value</span></span>

<span data-ttu-id="b04a9-111">Если функция завершается с ошибкой, функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b04a9-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="b04a9-112">Если функция не может выполнить вычисление, она возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="b04a9-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="b04a9-113">Используйте [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , чтобы вернуть ошибку в функцию проверки доступа.</span><span class="sxs-lookup"><span data-stu-id="b04a9-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="b04a9-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b04a9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04a9-115">**\_ \_ сведения о инициализации AUTHZ**</span><span class="sxs-lookup"><span data-stu-id="b04a9-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="b04a9-116">*аусзжетцентралакцессполицикаллбакк*</span><span class="sxs-lookup"><span data-stu-id="b04a9-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
