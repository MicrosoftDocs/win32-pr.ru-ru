---
description: Строки конструктора объектов COM+ — это строки инициализации, которые задаются администратором для компонента.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Основные понятия о строках конструктора объектов COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990463"
---
# <a name="com-object-constructor-strings-concepts"></a><span data-ttu-id="59885-103">Основные понятия о строках конструктора объектов COM+</span><span class="sxs-lookup"><span data-stu-id="59885-103">COM+ Object Constructor Strings Concepts</span></span>

<span data-ttu-id="59885-104">Строки конструктора объектов COM+ — это строки инициализации, которые задаются администратором для компонента.</span><span class="sxs-lookup"><span data-stu-id="59885-104">COM+ object constructor strings are initialization strings that are administratively specified for a component.</span></span> <span data-ttu-id="59885-105">Можно использовать строки конструктора объектов для записи одного компонента с степенью общего, позволяющей впоследствии настроить ее для конкретной задачи. то есть можно выполнить конструирование параметризованных объектов.</span><span class="sxs-lookup"><span data-stu-id="59885-105">You can use object constructor strings to write a single component with a degree of generality that allows it to be later customized for a particular task; that is, you can perform parameterized object construction.</span></span>

<span data-ttu-id="59885-106">Например, эту функцию можно использовать для записи компонента, содержащего Универсальное подключение ODBC, а позднее указать точное имя DSN для компонента в административном виде.</span><span class="sxs-lookup"><span data-stu-id="59885-106">For example, you might use this feature to write a component that holds a generic ODBC connection and later specify an exact DSN for the component administratively.</span></span> <span data-ttu-id="59885-107">При изменении конфигурации системы можно соответствующим образом изменить строку конструктора.</span><span class="sxs-lookup"><span data-stu-id="59885-107">If the system configuration changes, you can change the constructor string accordingly.</span></span>

> [!Note]  
> <span data-ttu-id="59885-108">Строки конструктора объектов не следует использовать для хранения конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="59885-108">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

<span data-ttu-id="59885-109">Вы можете использовать строки конструктора объектов в сочетании с [пулом объектов](com--object-pooling.md) для достижения большей степени детализации в способах пула и повторного использования ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59885-109">You can use object constructor strings in conjunction with [object pooling](com--object-pooling.md) to achieve a greater degree of granularity in how you pool and reuse resources.</span></span> <span data-ttu-id="59885-110">Например, можно создать несколько отдельных компонентов, идентичных, за исключением строк конструктора и идентификаторов CLSID, для поддержки различных пулов объектов, которые могут использовать соединения с отдельными группами клиентов.</span><span class="sxs-lookup"><span data-stu-id="59885-110">For example, you might create several distinct components, identical except for constructor strings and CLSIDs, to maintain distinct pools of objects holding connections usable by distinct groups of clients.</span></span> <span data-ttu-id="59885-111">Это может оказаться полезным, если соединения открываются способом, который привязывает их к определенным ролям безопасности, например, когда подключения открываются с определенной проверкой подлинности в базе данных, и их не рекомендуется использовать в общем случае.</span><span class="sxs-lookup"><span data-stu-id="59885-111">This would be useful if connections are opened in a manner that binds them to particular security roles—such as when the connections are opened with some specific authentication at the database—rendering them non-reusable in the general case.</span></span>

<span data-ttu-id="59885-112">Для этого можно написать один универсальный компонент, основанный на строках конструктора объектов, с помощью [**интерфейс IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct)и перекомпилировать его для создания нескольких настраиваемых компонентов с отдельным идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="59885-112">To do this, you can write a single generic component that relies on object constructor strings, using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), and recompile it to produce several customizable components each with a distinct CLSID.</span></span> <span data-ttu-id="59885-113">Затем можно самостоятельно адаптировать каждый компонент, чтобы открыть соответствующее соединение со строкой конструктора, настроить их для группировки в пул, и они будут храниться в разных пулах на каждый CLSID.</span><span class="sxs-lookup"><span data-stu-id="59885-113">You can then administratively tailor each component to open an appropriate connection with a constructor string, configure them to be pooled, and they will be maintained in distinct pools per CLSID.</span></span>

<span data-ttu-id="59885-114">Можно указать строку конструктора, если компонент был написан специально для распознавания введенной строки.</span><span class="sxs-lookup"><span data-stu-id="59885-114">You can specify a constructor string when a component has been written specifically to recognize the string that you enter.</span></span> <span data-ttu-id="59885-115">Компоненты могут получать доступ к этим строкам программным путем с помощью [**интерфейс IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span><span class="sxs-lookup"><span data-stu-id="59885-115">Components can access these strings programmatically by using [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).</span></span>

<span data-ttu-id="59885-116">Строки конструктора передаются во время создания объекта только при административном включении создания объектов.</span><span class="sxs-lookup"><span data-stu-id="59885-116">Constructor strings are passed in at object creation time only when object construction is administratively enabled.</span></span> <span data-ttu-id="59885-117">COM+ вызывает метод [**интерфейс IObjectConstruct:: конструирует**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) , который он реализует.</span><span class="sxs-lookup"><span data-stu-id="59885-117">COM+ calls the [**IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) method that it implements.</span></span> <span data-ttu-id="59885-118">В этом методе можно получить доступ к строке конструктора с помощью [**иобжектконструктстринг**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span><span class="sxs-lookup"><span data-stu-id="59885-118">Within that method, you can access the constructor string by using [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring).</span></span> <span data-ttu-id="59885-119">Пустые строки могут быть допустимыми записями.</span><span class="sxs-lookup"><span data-stu-id="59885-119">Empty strings can be valid entries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59885-120">См. также</span><span class="sxs-lookup"><span data-stu-id="59885-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59885-121">Группирование объектов COM+</span><span class="sxs-lookup"><span data-stu-id="59885-121">COM+ Object Pooling</span></span>](com--object-pooling.md)
</dt> <dt>

[<span data-ttu-id="59885-122">Указание строки конструктора объекта для компонента</span><span class="sxs-lookup"><span data-stu-id="59885-122">Specifying an Object Constructor String for a Component</span></span>](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[<span data-ttu-id="59885-123">Использование строки конструктора объекта для создания компонента</span><span class="sxs-lookup"><span data-stu-id="59885-123">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



