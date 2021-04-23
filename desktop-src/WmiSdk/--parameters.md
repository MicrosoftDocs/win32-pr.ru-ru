---
description: Определяет входные и выходные параметры для методов.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Класс __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693160"
---
# <a name="__parameters-class"></a><span data-ttu-id="45705-103">\_\_Класс параметров</span><span class="sxs-lookup"><span data-stu-id="45705-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="45705-104">Системный класс **\_ \_ параметров** — это абстрактный класс, который определяет входные и выходные параметры для методов.</span><span class="sxs-lookup"><span data-stu-id="45705-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="45705-105">Он также используется для передачи значений входных и выходных параметров между клиентом WMI и поставщиком метода.</span><span class="sxs-lookup"><span data-stu-id="45705-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="45705-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="45705-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="45705-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="45705-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45705-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45705-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="45705-109">Члены</span><span class="sxs-lookup"><span data-stu-id="45705-109">Members</span></span>

<span data-ttu-id="45705-110">Класс **\_ \_ параметров** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="45705-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="45705-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="45705-111">Remarks</span></span>

<span data-ttu-id="45705-112">Чтобы определить метод в пользовательском классе, клиент WMI создает копию класса **\_ \_ Parameters** и добавляет свойство для каждого входного параметра в методе.</span><span class="sxs-lookup"><span data-stu-id="45705-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="45705-113">Если метод содержит возвращаемое значение или выходные параметры, необходимо создать еще одну копию **\_ \_ параметров** .</span><span class="sxs-lookup"><span data-stu-id="45705-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="45705-114">Если метод возвращает возвращаемое значение, клиент должен добавить свойство с именем **ReturnValue**.</span><span class="sxs-lookup"><span data-stu-id="45705-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="45705-115">Затем поставщик метода сохраняет параметры метода с помощью вызова [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="45705-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="45705-116">Чтобы вызвать метод, клиент вызывает следующую последовательность:</span><span class="sxs-lookup"><span data-stu-id="45705-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="45705-117">[**Ивбемклассобжект::-Method**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) для получения копии класса **\_ \_ Parameters** , хранящегося в [**ивбемклассобжект::P утмесод**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="45705-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="45705-118">[**Ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), а затем устанавливает по одному свойству для каждого входного параметра в метод.</span><span class="sxs-lookup"><span data-stu-id="45705-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="45705-119">[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) или [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) для выполнения метода.</span><span class="sxs-lookup"><span data-stu-id="45705-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="45705-120">После завершения выполнения метода может возвращаться другой экземпляр класса **\_ \_ Parameters** , если метод имеет выходные параметры или возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="45705-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="45705-121">Если метод был вызван с помощью [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), то экземпляр **\_ \_ параметров** возвращается в качестве выходного аргумента.</span><span class="sxs-lookup"><span data-stu-id="45705-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="45705-122">Если метод был вызван с помощью [**IWbemServices:: ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), то экземпляр **\_ \_ параметров** возвращается в качестве параметра [**ивбемобжектсинк::**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="45705-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="45705-123">Требования</span><span class="sxs-lookup"><span data-stu-id="45705-123">Requirements</span></span>



| <span data-ttu-id="45705-124">Требование</span><span class="sxs-lookup"><span data-stu-id="45705-124">Requirement</span></span> | <span data-ttu-id="45705-125">Значение</span><span class="sxs-lookup"><span data-stu-id="45705-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="45705-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45705-126">Minimum supported client</span></span><br/> | <span data-ttu-id="45705-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45705-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="45705-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45705-128">Minimum supported server</span></span><br/> | <span data-ttu-id="45705-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45705-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="45705-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="45705-130">Namespace</span></span><br/>                | <span data-ttu-id="45705-131">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="45705-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="45705-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45705-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45705-133">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="45705-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="45705-134">**IWbemServices:: Ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="45705-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="45705-135">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="45705-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




