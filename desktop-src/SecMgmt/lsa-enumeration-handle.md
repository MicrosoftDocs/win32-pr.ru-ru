---
description: '\_ \_ Тип данных Handle для перечисления LSA используется функцией LSA, которая перечисляет объекты Трустеддомаин: лсаенумератетрустеддомаинсекс.'
ms.assetid: 99dad3aa-cb92-4b7e-8a18-2c977cb2737c
title: LSA_ENUMERATION_HANDLE (Нтсекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db71e9522a188956a7aa838b11ba74f08bde39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683480"
---
# <a name="lsa_enumeration_handle"></a><span data-ttu-id="18bd1-103">\_обработчик ПЕРЕЧИСЛЕНИЯ \_ LSA</span><span class="sxs-lookup"><span data-stu-id="18bd1-103">LSA\_ENUMERATION\_HANDLE</span></span>

<span data-ttu-id="18bd1-104">Тип **данных \_ \_ Handle для перечисления LSA** используется функцией LSA, которая перечисляет объекты [**трустеддомаин**](trusteddomain-object.md) : [**лсаенумератетрустеддомаинсекс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="18bd1-104">The **LSA\_ENUMERATION\_HANDLE** data type is used by the LSA function that enumerates [**TrustedDomain**](trusteddomain-object.md) objects: [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span> <span data-ttu-id="18bd1-105">Эта функция разработана таким образом, чтобы можно было выполнять несколько вызовов для перечисления всех объектов заданного типа в базе данных.</span><span class="sxs-lookup"><span data-stu-id="18bd1-105">This function is designed so that you can make multiple calls to enumerate all the objects of a given type in the database.</span></span>

<span data-ttu-id="18bd1-106">При вызове функции начального перечисления вы передаете указатель на переменную **\_ \_ обработчика для перечисления LSA** , которая инициализируется значением 0.</span><span class="sxs-lookup"><span data-stu-id="18bd1-106">On the initial enumeration function call, you pass in a pointer to an **LSA\_ENUMERATION\_HANDLE** variable that is initialized to zero.</span></span> <span data-ttu-id="18bd1-107">Функция обновляет это значение.</span><span class="sxs-lookup"><span data-stu-id="18bd1-107">The function updates this value.</span></span> <span data-ttu-id="18bd1-108">Если функция возвращает значение, указывающее, что для перечисления больше объектов, вызовите функцию еще раз и передайте обновленное значение **\_ \_ обработчика перечисления LSA** , чтобы получить перечисление, продолжая с точки, где предыдущее перечисление было оставлено отключенным.</span><span class="sxs-lookup"><span data-stu-id="18bd1-108">If the function returns a value that indicates there are more objects to enumerate, call the function again and pass in the updated **LSA\_ENUMERATION\_HANDLE** value to obtain an enumeration continuing from the point where the previous enumeration left off.</span></span>


```C++
typedef ULONG LSA_ENUMERATION_HANDLE, *PLSA_ENUMERATION_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="18bd1-109">Требования</span><span class="sxs-lookup"><span data-stu-id="18bd1-109">Requirements</span></span>



| <span data-ttu-id="18bd1-110">Требование</span><span class="sxs-lookup"><span data-stu-id="18bd1-110">Requirement</span></span> | <span data-ttu-id="18bd1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="18bd1-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18bd1-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="18bd1-112">Minimum supported client</span></span><br/> | <span data-ttu-id="18bd1-113">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="18bd1-113">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18bd1-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="18bd1-114">Minimum supported server</span></span><br/> | <span data-ttu-id="18bd1-115">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="18bd1-115">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="18bd1-116">Header</span><span class="sxs-lookup"><span data-stu-id="18bd1-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="18bd1-117"><dt>Нтсекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="18bd1-117"><dt>Ntsecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18bd1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="18bd1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18bd1-119">**лсаенумератетрустеддомаинсекс**</span><span class="sxs-lookup"><span data-stu-id="18bd1-119">**LsaEnumerateTrustedDomainsEx**</span></span>](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)
</dt> </dl>

 

 




