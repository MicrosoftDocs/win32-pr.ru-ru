---
description: Интерфейс Инонделегатингункновн — это версия IUnknown, которая переименовывается, чтобы обеспечить поддержку как для неделегирования, так и для делегирования интерфейсов IUnknown в одном COM-объекте.
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: Инонделегатингункновн (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 13e93d5ba083706ee361addeb4db2157471cbe25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679750"
---
# <a name="inondelegatingunknown"></a><span data-ttu-id="1e5bd-103">инонделегатингункновн</span><span class="sxs-lookup"><span data-stu-id="1e5bd-103">INonDelegatingUnknown</span></span>

<span data-ttu-id="1e5bd-104">`INonDelegatingUnknown`Интерфейс — это версия **IUnknown** , которая переименовывается, чтобы обеспечить поддержку как неделегирования, так и делегирования интерфейсов **IUnknown** в одном COM-объекте.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-104">The `INonDelegatingUnknown` interface is a version of **IUnknown** that is renamed to enable support for both nondelegating and delegating **IUnknown** interfaces in the same COM object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e5bd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e5bd-105">Syntax</span></span>


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a><span data-ttu-id="1e5bd-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e5bd-106">Remarks</span></span>

<span data-ttu-id="1e5bd-107">Чтобы использовать `INonDelegatingUnknown` для множественного наследования, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-107">To use `INonDelegatingUnknown` for multiple inheritance, perform the following steps.</span></span>

1.  <span data-ttu-id="1e5bd-108">Создайте класс, производный от интерфейса, например IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-108">Derive your class from an interface, for example, IMyInterface.</span></span>
2.  <span data-ttu-id="1e5bd-109">Включите [**объявление \_ IUnknown**](declare-iunknown.md) в определение класса, чтобы объявить реализации **QueryInterface**, **AddRef** и **Release** , которые вызывают внешнюю неизвестную функцию.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-109">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition to declare implementations of **QueryInterface**, **AddRef**, and **Release** that call the outer unknown.</span></span>
3.  <span data-ttu-id="1e5bd-110">Переопределите **нонделегатингкуеринтерфаце** , чтобы предоставить IMyInterface с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="1e5bd-110">Override **NonDelegatingQueryInterface** to expose IMyInterface with code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="1e5bd-111">Объявите и реализуйте функции элементов IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-111">Declare and implement the member functions of IMyInterface.</span></span>

<span data-ttu-id="1e5bd-112">Чтобы использовать `INonDelegatingUnknown` для вложенных интерфейсов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-112">To use `INonDelegatingUnknown` for nested interfaces, perform the following steps:</span></span>

1.  <span data-ttu-id="1e5bd-113">Объявите класс, производный от [**кункновн**](cunknown.md).</span><span class="sxs-lookup"><span data-stu-id="1e5bd-113">Declare a class derived from [**CUnknown**](cunknown.md).</span></span>
2.  <span data-ttu-id="1e5bd-114">Включите [**объявление \_ IUnknown**](declare-iunknown.md) в определение класса.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-114">Include [**DECLARE\_IUNKNOWN**](declare-iunknown.md) in your class definition.</span></span>
3.  <span data-ttu-id="1e5bd-115">Переопределите **нонделегатингкуеринтерфаце** , чтобы предоставить IMyInterface с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="1e5bd-115">Override **NonDelegatingQueryInterface** to expose IMyInterface with the code such as the following:</span></span>
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  <span data-ttu-id="1e5bd-116">Реализуйте функции члена IMyInterface.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-116">Implement the member functions of IMyInterface.</span></span> <span data-ttu-id="1e5bd-117">Используйте [**кункновн::-owner**](cunknown-getowner.md) для доступа к классу COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-117">Use [**CUnknown::GetOwner**](cunknown-getowner.md) to access the COM object class.</span></span>
5.  <span data-ttu-id="1e5bd-118">В классе COM-объекта сделайте вложенный класс дружественным классом COM-объекта и объявите экземпляр вложенного класса как член класса COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-118">In your COM object class, make the nested class a friend of the COM object class, and declare an instance of the nested class as a member of the COM object class.</span></span>

<span data-ttu-id="1e5bd-119">Поскольку необходимо всегда передавать внешнее неизвестное значение и **HRESULT** в конструктор [**кункновн**](cunknown.md) , нельзя использовать конструктор по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-119">Because you must always pass the outer unknown and an **HRESULT** to the [**CUnknown**](cunknown.md) constructor, you can't use a default constructor.</span></span> <span data-ttu-id="1e5bd-120">Необходимо сделать переменную-член указателем на класс и создать новый вызов в конструкторе, чтобы создать его.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-120">You have to make the member variable a pointer to the class and make a new call in your constructor to actually create it.</span></span>

<span data-ttu-id="1e5bd-121">Переопределите **нонделегатингкуеринтерфаце** с помощью следующего кода:</span><span class="sxs-lookup"><span data-stu-id="1e5bd-121">Override the **NonDelegatingQueryInterface** with code such as the following:</span></span>


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



<span data-ttu-id="1e5bd-122">Можно использовать смешанные классы, поддерживающие некоторые интерфейсы посредством нескольких наследования и некоторых интерфейсов через вложенные классы.</span><span class="sxs-lookup"><span data-stu-id="1e5bd-122">You can have mixed classes that support some interfaces through multiple inheritance and some interfaces through nested classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e5bd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1e5bd-123">Requirements</span></span>



| <span data-ttu-id="1e5bd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1e5bd-124">Requirement</span></span> | <span data-ttu-id="1e5bd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1e5bd-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e5bd-126">Header</span><span class="sxs-lookup"><span data-stu-id="1e5bd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1e5bd-127"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e5bd-127"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e5bd-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1e5bd-128">Library</span></span><br/> | <dl> <span data-ttu-id="1e5bd-129"><dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt></span><span class="sxs-lookup"><span data-stu-id="1e5bd-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e5bd-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e5bd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e5bd-131">**Вспомогательные функции COM**</span><span class="sxs-lookup"><span data-stu-id="1e5bd-131">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




