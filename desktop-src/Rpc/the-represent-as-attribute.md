---
title: Атрибут represent_as
description: Атрибут \ представить \_ как \ позволяет указать, каким образом в приложение будет представлен конкретный тип данных для передачи.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- Удаленный вызов процедур RPC, атрибуты, represent_as
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134458"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="3d67e-105">Атрибут представления \_ как</span><span class="sxs-lookup"><span data-stu-id="3d67e-105">The represent\_as Attribute</span></span>

<span data-ttu-id="3d67e-106">Атрибут \[ [представить \_ как](/windows/desktop/Midl/represent-as) \] позволяет указать, каким образом в приложение будет представлен конкретный тип данных для передачи.</span><span class="sxs-lookup"><span data-stu-id="3d67e-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="3d67e-107">Для этого нужно указать имя представленного типа для известного типа передающего объекта и предоставить подпрограммы преобразования.</span><span class="sxs-lookup"><span data-stu-id="3d67e-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="3d67e-108">Кроме того, необходимо предоставить подпрограммы для высвобождения памяти, используемой объектами типа данных.</span><span class="sxs-lookup"><span data-stu-id="3d67e-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="3d67e-109">Используйте атрибут **\[ представить \_ как \]** для представления приложения с другим, возможно, недопустимым типом данных, а не типом, который фактически передается между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="3d67e-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="3d67e-110">Также возможно, что тип, который манипулирует приложением, может быть неизвестным во время компиляции MIDL.</span><span class="sxs-lookup"><span data-stu-id="3d67e-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="3d67e-111">При выборе хорошо определенного типа, передающего данные, не стоит беспокоиться о представлении данных в разнородной среде.</span><span class="sxs-lookup"><span data-stu-id="3d67e-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="3d67e-112">Атрибут « **\[ представить \_ как \]** » может сделать приложение более эффективным, уменьшая объем данных, передаваемых по сети.</span><span class="sxs-lookup"><span data-stu-id="3d67e-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="3d67e-113">Атрибут « **\[ представить \_ как \]** » аналогичен \[ атрибуту « [передать \_ как](/windows/desktop/Midl/transmit-as) » \] .</span><span class="sxs-lookup"><span data-stu-id="3d67e-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="3d67e-114">Однако при **\[ передаче \_ как \]** позволяет указать тип данных, который будет использоваться для передачи, **\[ представляется \_ как \]** позволяет указать, как тип данных представлен для приложения.</span><span class="sxs-lookup"><span data-stu-id="3d67e-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="3d67e-115">Представленный тип не требуется определять в файлах, обработанных MIDL; его можно определить во время компиляции заглушек с помощью компилятора C.</span><span class="sxs-lookup"><span data-stu-id="3d67e-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="3d67e-116">Для этого используйте директиву include в [файле конфигурации приложения (ACF)](the-application-configuration-file-acf-.md) , чтобы скомпилировать соответствующий файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="3d67e-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="3d67e-117">Например, следующий ACF определяет тип, локальный для приложения, **\_ тип репр**, для типа, поддающегося типу, **с именем \_ Type:**</span><span class="sxs-lookup"><span data-stu-id="3d67e-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="3d67e-118">В следующей таблице описаны четыре подпрограммы, предоставляемые программистом.</span><span class="sxs-lookup"><span data-stu-id="3d67e-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="3d67e-119">Подпрограмма</span><span class="sxs-lookup"><span data-stu-id="3d67e-119">Routine</span></span>                      | <span data-ttu-id="3d67e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="3d67e-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d67e-121">**именованный \_ тип \_ из \_ локальной**</span><span class="sxs-lookup"><span data-stu-id="3d67e-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="3d67e-122">Выделяет экземпляр типа сети и выполняет преобразование из локального типа в тип сети.</span><span class="sxs-lookup"><span data-stu-id="3d67e-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="3d67e-123">**именованный \_ тип \_ в \_ Local**</span><span class="sxs-lookup"><span data-stu-id="3d67e-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="3d67e-124">Преобразует тип сети в локальный тип.</span><span class="sxs-lookup"><span data-stu-id="3d67e-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="3d67e-125">**\_ \_ свободный \_ локальный именованный тип**</span><span class="sxs-lookup"><span data-stu-id="3d67e-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="3d67e-126">Освобождает память, выделенную с помощью вызова **именованного \_ типа, \_ в \_ локальную** подпрограммы, но не сам тип.</span><span class="sxs-lookup"><span data-stu-id="3d67e-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="3d67e-127">**\_ \_ свободный \_ inst именованного типа**</span><span class="sxs-lookup"><span data-stu-id="3d67e-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="3d67e-128">Освобождает хранилище для типа сети (по обеим сторонам).</span><span class="sxs-lookup"><span data-stu-id="3d67e-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="3d67e-129">В отличие от этих четырех подпрограмм, предоставленных программистом, именованный тип не обрабатывается приложением.</span><span class="sxs-lookup"><span data-stu-id="3d67e-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="3d67e-130">Единственным типом, видимым для приложения, является представленный тип.</span><span class="sxs-lookup"><span data-stu-id="3d67e-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="3d67e-131">Приложение использует имя представленного типа вместо имени переданного типа в прототипах и заглушках, созданных компилятором.</span><span class="sxs-lookup"><span data-stu-id="3d67e-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="3d67e-132">Необходимо указать набор подпрограмм для обеих сторон.</span><span class="sxs-lookup"><span data-stu-id="3d67e-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="3d67e-133">Для временных объектов **именованного \_ типа** заглушка вызывает **именованный \_ тип \_ Free \_ inst** , чтобы освободить память, выделенную вызовом **именованного \_ типа \_ из \_ локальной** переменной.</span><span class="sxs-lookup"><span data-stu-id="3d67e-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="3d67e-134">Если представленный тип является указателем или содержит указатель, **именованный \_ тип \_ в \_ локальную** подпрограмму должен выделять память для данных, к которым точка указателя (объект представленного типа управляется заглушкой обычным способом).</span><span class="sxs-lookup"><span data-stu-id="3d67e-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="3d67e-135">Для \[ [out](/windows/desktop/Midl/out-idl) \] и \[ [in](/windows/desktop/Midl/in)выходные \] Параметры типа, которые содержат элементы **\[ представления \_ как** или один из его компонентов, для объектов данных, содержащих атрибут, автоматически вызывается **\_ \_ \_ Локальная подпрограммы с именованным типом Free** .</span><span class="sxs-lookup"><span data-stu-id="3d67e-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="3d67e-136">Для **\[ \] входных** параметров **\_ \_ \_ Локальная подпрограммы с именованным типом** вызывается, только если к параметру применен атрибут " **\[ представить \_ как \]** ".</span><span class="sxs-lookup"><span data-stu-id="3d67e-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="3d67e-137">Если атрибут применен к компонентам параметра, то не вызывается *\* \*\*\* \_ бесплатная \_ Локальная* подпрограммы \*.</span><span class="sxs-lookup"><span data-stu-id="3d67e-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="3d67e-138">Свободные подпрограммы не вызываются для внедренных данных и параллельного вызова (связанного с атрибутом верхнего уровня) для параметра только **\[ в \]** .</span><span class="sxs-lookup"><span data-stu-id="3d67e-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="3d67e-139">К одному и тому же типу можно применить как атрибуты **\[ передачи \_ \]** , так и **\[ представления \_ \]** .</span><span class="sxs-lookup"><span data-stu-id="3d67e-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="3d67e-140">При упаковке данных сначала применяется преобразование типа **\[ представления \_ как \]** тип, а затем применяется преобразование « **\[ Передача \_ как \]** ».</span><span class="sxs-lookup"><span data-stu-id="3d67e-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="3d67e-141">При демаршалировании данных порядок изменяется в противоположный.</span><span class="sxs-lookup"><span data-stu-id="3d67e-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="3d67e-142">Таким словами, при упаковке \* **\_ из \_ локальной** области выделяется экземпляр именованного типа, который преобразуется из объекта локального типа в объект временного именованного типа.</span><span class="sxs-lookup"><span data-stu-id="3d67e-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="3d67e-143">Этот объект представляет собой представленный объект типа, используемый для \* подпрограммы **\_ to \_ xmit** .</span><span class="sxs-lookup"><span data-stu-id="3d67e-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="3d67e-144">\*Затем подпрограммы **\_ to \_ xmit** распределяют переданный объект типа и переводит его из представленного (именованного) объекта в переданный объект.</span><span class="sxs-lookup"><span data-stu-id="3d67e-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="3d67e-145">Для представления связанного списка можно использовать массив длинных целых чисел.</span><span class="sxs-lookup"><span data-stu-id="3d67e-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="3d67e-146">Таким образом, приложение обрабатывает список, а передача использует массив длинных целых чисел при передаче списка этого типа.</span><span class="sxs-lookup"><span data-stu-id="3d67e-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="3d67e-147">Можно начать с массива, но более удобно использовать конструкцию с открытым массивом длинных целых чисел.</span><span class="sxs-lookup"><span data-stu-id="3d67e-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="3d67e-148">В приведенном ниже примере показано, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="3d67e-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="3d67e-149">Обратите внимание, что прототипы подпрограмм, использующих тип **лонгарр** , фактически отображаются в файле заглушек. h в качестве **Плок \_** вместо типа **лонгарр** .</span><span class="sxs-lookup"><span data-stu-id="3d67e-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="3d67e-150">То же самое справедливо и для соответствующих заглушек в файле заглушки \_ c. c.</span><span class="sxs-lookup"><span data-stu-id="3d67e-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="3d67e-151">Необходимо указать следующие четыре функции:</span><span class="sxs-lookup"><span data-stu-id="3d67e-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="3d67e-152">Приведенные выше подпрограммы выполняют следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3d67e-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="3d67e-153">**Лонгарр \_ из \_ локальной** подпрограммы подсчитывает узлы списка, выделяет объект лонгарр с размером **sizeof**(**лонгарр**) + Count \* **sizeof**(**Long**), устанавливает в поле **size** значение Count и копирует данные в поле **датаарр** .</span><span class="sxs-lookup"><span data-stu-id="3d67e-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="3d67e-154">**Лонгарр \_ to \_ Local** подпрограммы создает список с размерами узлов и передает массив соответствующим узлам.</span><span class="sxs-lookup"><span data-stu-id="3d67e-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="3d67e-155">Подпрограммы **лонгарр \_ Free \_ inst** в этом случае не освобождаются.</span><span class="sxs-lookup"><span data-stu-id="3d67e-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="3d67e-156">**\_ Бесплатная \_ Локальная** подпрограммы лонгарр освобождает все узлы списка.</span><span class="sxs-lookup"><span data-stu-id="3d67e-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 