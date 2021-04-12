---
title: Создание глобальной таблицы интерфейса
description: Создание глобальной таблицы интерфейса
ms.assetid: e8e46642-ef41-4322-97d0-8dd5b7c72992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f792f9664da554f6522086796f94a00ccdf0dc07
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413877"
---
# <a name="creating-the-global-interface-table"></a><span data-ttu-id="2191a-103">Создание глобальной таблицы интерфейса</span><span class="sxs-lookup"><span data-stu-id="2191a-103">Creating the Global Interface Table</span></span>

<span data-ttu-id="2191a-104">Используйте следующий вызов, чтобы создать объект таблицы глобальных интерфейсов и получить указатель на [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span><span class="sxs-lookup"><span data-stu-id="2191a-104">Use the following call to create the global interface table object and get a pointer to [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable):</span></span>

``` syntax
HRESULT hr;
hr = CoCreateInstance(CLSID_StdGlobalInterfaceTable,
                 NULL,
                 CLSCTX_INPROC_SERVER,
                 IID_IGlobalInterfaceTable,
                 (void **)&gpGIT);
if (hr != S_OK) {
  exit(0); // Handle errors here.
}
```

> [!Note]  
> <span data-ttu-id="2191a-105">При создании объекта глобальной таблицы интерфейса с помощью предыдущего вызова необходимо создать ссылку на библиотеку UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="2191a-105">When creating the global interface table object using the preceding call, it is necessary to link to the library uuid.lib.</span></span> <span data-ttu-id="2191a-106">Это позволит разрешить внешние символы CLSID \_ стдглобалинтерфацетабле и IID \_ иглобалинтерфацетабле.</span><span class="sxs-lookup"><span data-stu-id="2191a-106">This will resolve the external symbols CLSID\_StdGlobalInterfaceTable and IID\_IGlobalInterfaceTable.</span></span>

 

<span data-ttu-id="2191a-107">Для каждого процесса существует единственный экземпляр глобальной таблицы интерфейса, поэтому все вызовы этой функции в процессе возвращают один и тот же экземпляр.</span><span class="sxs-lookup"><span data-stu-id="2191a-107">There is a single instance of the global interface table per process, so all calls to this function in a process return the same instance.</span></span>

<span data-ttu-id="2191a-108">После вызова функции [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Зарегистрируйте интерфейс в подразделении, в котором он находится, с помощью вызова метода [**регистеринтерфацеинглобал**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) .</span><span class="sxs-lookup"><span data-stu-id="2191a-108">After the call to the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function, register the interface from the apartment in which it resides with a call to the [**RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) method.</span></span> <span data-ttu-id="2191a-109">Этот метод предоставляет файл cookie, определяющий интерфейс и его расположение.</span><span class="sxs-lookup"><span data-stu-id="2191a-109">This method supplies a cookie that identifies the interface and its location.</span></span> <span data-ttu-id="2191a-110">Апартамент, который ищет указатель на этот интерфейс, затем вызывает метод [**жетинтерфацефромглобал**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) с этим файлом cookie, а реализация затем предоставляет указатель интерфейса на вызывающий апартамент.</span><span class="sxs-lookup"><span data-stu-id="2191a-110">An apartment seeking a pointer to this interface then calls the [**GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal) method with this cookie, and the implementation then supplies an interface pointer to the calling apartment.</span></span> <span data-ttu-id="2191a-111">Чтобы отозвать глобальную регистрацию интерфейса, любой апартамент может вызвать метод [**ревокеинтерфацефромглобал**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) .</span><span class="sxs-lookup"><span data-stu-id="2191a-111">To revoke the interface's global registration, any apartment can call the [**RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) method.</span></span>

<span data-ttu-id="2191a-112">Простым примером использования [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) является то, что необходимо передать указатель интерфейса на объект в однопотоковом апартаменте (STA) в рабочий поток в другом апартаменте.</span><span class="sxs-lookup"><span data-stu-id="2191a-112">A simple example of using [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) would be when you want to pass an interface pointer on an object in a single-threaded apartment (STA) to a worker thread in another apartment.</span></span> <span data-ttu-id="2191a-113">Вместо того, чтобы выполнять упаковку в поток и передавать поток рабочему потоку в качестве параметра потока, **иглобалинтерфацетабле** позволяет просто передать файл cookie.</span><span class="sxs-lookup"><span data-stu-id="2191a-113">Rather than having to marshal it into a stream and pass the stream to the worker thread as a thread parameter, **IGlobalInterfaceTable** allows you simply to pass a cookie.</span></span>

<span data-ttu-id="2191a-114">При регистрации интерфейса в глобальной таблице интерфейсов вы получаете файл cookie, который можно использовать вместо передачи фактического указателя (при необходимости передачи указателя) либо в параметр, не являющийся методом, который переходит в другой апартамент (в качестве параметра [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) через [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)), либо на внутрипроцессный объем памяти, доступный за пределами подразделения.</span><span class="sxs-lookup"><span data-stu-id="2191a-114">When you register the interface in the global interface table, you get a cookie that you can use instead of passing the actual pointer (whenever you need to pass the pointer), either to a nonmethod parameter that is going to another apartment (as a parameter to [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85)) through [**CreateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread)) or to in-process memory accessible outside your apartment.</span></span>

<span data-ttu-id="2191a-115">Необходимо соблюдать осторожность, так как использование глобальных интерфейсов полагается на программиста по управлению такими проблемами, как конкуренция и взаимное исключение, связанные с доступом к глобальному состоянию из нескольких потоков одновременно.</span><span class="sxs-lookup"><span data-stu-id="2191a-115">Care is required because using global interfaces places the extra burden on the programmer of managing problems such as race conditions and mutual exclusion, which are associated with accessing global state from multiple threads simultaneously.</span></span>

<span data-ttu-id="2191a-116">COM предоставляет стандартную реализацию интерфейса [**иглобалинтерфацетабле**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) .</span><span class="sxs-lookup"><span data-stu-id="2191a-116">COM provides a standard implementation of the [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) interface.</span></span> <span data-ttu-id="2191a-117">Настоятельно рекомендуется использовать эту стандартную реализацию, так как она предоставляет полноценные потокобезопасные функции.</span><span class="sxs-lookup"><span data-stu-id="2191a-117">It is highly recommended that you use this standard implementation because it provides complete thread-safe functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2191a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="2191a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2191a-119">Когда следует использовать глобальную таблицу интерфейса</span><span class="sxs-lookup"><span data-stu-id="2191a-119">When to Use the Global Interface Table</span></span>](when-to-use-the-global-interface-table.md)
</dt> </dl>

 

 