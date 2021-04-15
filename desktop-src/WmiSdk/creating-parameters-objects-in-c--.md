---
description: 'Для методов IWbemServices:: ExecMethod или Ексекмесодасинк требуется \_ \_ системный класс Parameters в качестве контейнера в пинпарамс, если у метода, который они выполняют, есть входные аргументы.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Создание объектов параметров в C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263938"
---
# <a name="creating-parameters-objects-in-c"></a><span data-ttu-id="e93a5-103">Создание объектов параметров в C++</span><span class="sxs-lookup"><span data-stu-id="e93a5-103">Creating Parameters Objects in C++</span></span>

<span data-ttu-id="e93a5-104">Для методов [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) или [**ексекмесодасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) требуется системный класс [**\_ \_ Parameters**](--parameters.md) в качестве контейнера в *пинпарамс* , если у метода, который они выполняют, есть входные аргументы.</span><span class="sxs-lookup"><span data-stu-id="e93a5-104">The [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) methods require the [**\_\_PARAMETERS**](--parameters.md) system class as a container in *pInParams* if the method they are executing has any input arguments.</span></span>

<span data-ttu-id="e93a5-105">В следующей процедуре описывается создание экземпляра системного класса [**\_ \_ Parameters**](--parameters.md) для хранения сведений о параметрах.</span><span class="sxs-lookup"><span data-stu-id="e93a5-105">The following procedure describes how to create an instance of the [**\_\_PARAMETERS**](--parameters.md) system class to hold parameter information.</span></span>

<span data-ttu-id="e93a5-106">**Создание экземпляра \_ \_ параметров**</span><span class="sxs-lookup"><span data-stu-id="e93a5-106">**To create an instance of \_\_PARAMETERS**</span></span>

1.  <span data-ttu-id="e93a5-107">Определите путь к классу для класса, содержащего определение метода.</span><span class="sxs-lookup"><span data-stu-id="e93a5-107">Determine the class path for the class containing the method definition.</span></span>
2.  <span data-ttu-id="e93a5-108">С помощью пути к классу и аргумента [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , переданного из метода [**Ивбемпровидеринит:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), вызовите [**ивбемклассобжект:: Method**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) , чтобы получить классы входных и выходных параметров.</span><span class="sxs-lookup"><span data-stu-id="e93a5-108">Using the class path and the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer passed in from [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), call [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve the input and output parameter classes.</span></span>

    <span data-ttu-id="e93a5-109">Метод метода [**WebMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) возвращает указатель [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) для доступа к каждому из этих классов.</span><span class="sxs-lookup"><span data-stu-id="e93a5-109">The [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for accessing each of these classes.</span></span>

3.  <span data-ttu-id="e93a5-110">С помощью указателя [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) для выходного класса вызовите [**Ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) , чтобы создать экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="e93a5-110">Using the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer for the output class, call [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) to create an instance of the class.</span></span>
4.  <span data-ttu-id="e93a5-111">Заполните экземпляр класса, задав свойства, соответствующие выходным значениям, и, если имеется возвращаемое значение для метода, свойство [ReturnValue](creating-a-method.md) .</span><span class="sxs-lookup"><span data-stu-id="e93a5-111">Populate the class instance by setting the properties that correspond to the output values and, if there is a return value for the method, the [ReturnValue](creating-a-method.md) property.</span></span>
5.  <span data-ttu-id="e93a5-112">Передайте экземпляр [**\_ \_ параметров**](--parameters.md) обратно вызывающему объекту через метод [**ивбемобжектсинк:: обозначают**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .</span><span class="sxs-lookup"><span data-stu-id="e93a5-112">Pass the [**\_\_PARAMETERS**](--parameters.md) instance back to the caller through the [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) method.</span></span>

<span data-ttu-id="e93a5-113">После того как поставщик метода определит, что входные параметры верны, метод, на который указывает *стрмесоднаме* , может по-прежнему пройти или завершиться неудачно.</span><span class="sxs-lookup"><span data-stu-id="e93a5-113">After a method provider determines that the input parameters are correct, the method pointed to by *strMethodName* might still pass or fail.</span></span> <span data-ttu-id="e93a5-114">Некоторые поставщики методов порождают второй поток для реализации метода, чтобы фактический успех или неудача выполнения метода был передан вызывающему объекту через [**ивбемобжектсинк:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span><span class="sxs-lookup"><span data-stu-id="e93a5-114">Some method providers spawn a second thread to implement the method so that the method's actual success or failure ends up being reported to the caller through [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).</span></span> <span data-ttu-id="e93a5-115">Обратите внимание, что **ивбемобжектсинк:: SetStatus** не получает код возврата метода поставщика.</span><span class="sxs-lookup"><span data-stu-id="e93a5-115">Note that **IWbemObjectSink::SetStatus** does not receive the return code of the provider method.</span></span> <span data-ttu-id="e93a5-116">Однако он получает код возврата фактического механизма возврата вызовов, и его удобно использовать только для проверки того, что вызов произошел, или что его не удалось выполнить по механическим причинам.</span><span class="sxs-lookup"><span data-stu-id="e93a5-116">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e93a5-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e93a5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e93a5-118">Вызов метода</span><span class="sxs-lookup"><span data-stu-id="e93a5-118">Calling a Method</span></span>](calling-a-method.md)
</dt> <dt>

[<span data-ttu-id="e93a5-119">**Ивбемкаллресулт:: Жетресултобжект**</span><span class="sxs-lookup"><span data-stu-id="e93a5-119">**IWbemCallResult::GetResultObject**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[<span data-ttu-id="e93a5-120">**IWbemServices:: Ексекмесодасинк**</span><span class="sxs-lookup"><span data-stu-id="e93a5-120">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="e93a5-121">**IWbemServices:: ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="e93a5-121">**IWbemServices::ExecMethod**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



