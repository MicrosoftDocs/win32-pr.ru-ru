---
description: Обработчик для объекта локальной политики.
ms.assetid: f5878d27-558b-4ef1-9401-1277e740c61d
title: LSA_HANDLE (Нтсекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07bd71a14666dde7bb92e439159a55dd71706612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080843"
---
# <a name="lsa_handle"></a><span data-ttu-id="3fa24-103">LSA \_ Handle</span><span class="sxs-lookup"><span data-stu-id="3fa24-103">LSA\_HANDLE</span></span>

<span data-ttu-id="3fa24-104">Тип **данных \_ обработчика LSA** — это обработчик локального объекта [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa24-104">The **LSA\_HANDLE** data type is a handle to the local [**Policy**](policy-object.md) object.</span></span>


```C++
typedef PVOID LSA_HANDLE, *PLSA_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="3fa24-105">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fa24-105">Remarks</span></span>

<span data-ttu-id="3fa24-106">Прежде чем использовать интерфейс локальной политики API, приложение должно открыть обработчик для объекта [**политики**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa24-106">Before you can use the local policy API your application must open a handle to a [**Policy**](policy-object.md) object.</span></span> <span data-ttu-id="3fa24-107">Для этого вызовите [**лсаопенполици**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span><span class="sxs-lookup"><span data-stu-id="3fa24-107">To do this, call [**LsaOpenPolicy**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy).</span></span> <span data-ttu-id="3fa24-108">Эта функция возвращает маркер, который приложение может указать в последующих вызовах функции политики LSA.</span><span class="sxs-lookup"><span data-stu-id="3fa24-108">This function returns a handle that your application can then specify in subsequent LSA policy function calls.</span></span>

<span data-ttu-id="3fa24-109">Каждый обработчик имеет связанный набор разрешений, определяющий операции, которые приложение может выполнять над объектом [**политики**](policy-object.md) с помощью этого маркера.</span><span class="sxs-lookup"><span data-stu-id="3fa24-109">Each handle has an associated set of permissions that determine the operations your application can perform on the [**Policy**](policy-object.md) object by using the handle.</span></span> <span data-ttu-id="3fa24-110">Приложение может одновременно открыть более одного маркера для объекта **политики** .</span><span class="sxs-lookup"><span data-stu-id="3fa24-110">Your application can open more than one handle to the **Policy** object at a time.</span></span> <span data-ttu-id="3fa24-111">Если маркер больше не требуется, приложение должно закрыть его, вызвав [**лсаклосе**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span><span class="sxs-lookup"><span data-stu-id="3fa24-111">When a handle is no longer required, your application should close it by calling [**LsaClose**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa24-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3fa24-112">Requirements</span></span>



| <span data-ttu-id="3fa24-113">Требование</span><span class="sxs-lookup"><span data-stu-id="3fa24-113">Requirement</span></span> | <span data-ttu-id="3fa24-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3fa24-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa24-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fa24-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa24-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3fa24-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3fa24-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fa24-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa24-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fa24-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fa24-119">Header</span><span class="sxs-lookup"><span data-stu-id="3fa24-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fa24-120"><dt>Нтсекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa24-120"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa24-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fa24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa24-122">**лсаклосе**</span><span class="sxs-lookup"><span data-stu-id="3fa24-122">**LsaClose**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaclose)
</dt> <dt>

[<span data-ttu-id="3fa24-123">**лсаопенполици**</span><span class="sxs-lookup"><span data-stu-id="3fa24-123">**LsaOpenPolicy**</span></span>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaopenpolicy)
</dt> </dl>

 

