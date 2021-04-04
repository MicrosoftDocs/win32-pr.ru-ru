---
description: В таблице Каунтердетаилс описывается конкретный счетчик на определенном компьютере.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: каунтердетаилс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998530"
---
# <a name="counterdetails"></a><span data-ttu-id="81d3c-103">каунтердетаилс</span><span class="sxs-lookup"><span data-stu-id="81d3c-103">CounterDetails</span></span>

<span data-ttu-id="81d3c-104">В таблице **каунтердетаилс** описывается конкретный счетчик на определенном компьютере.</span><span class="sxs-lookup"><span data-stu-id="81d3c-104">The **CounterDetails** table describes a specific counter on a particular computer.</span></span>

<span data-ttu-id="81d3c-105">В таблице **каунтердетаилс** определены следующие поля:</span><span class="sxs-lookup"><span data-stu-id="81d3c-105">The **CounterDetails** table defines the following fields:</span></span>

-   <span data-ttu-id="81d3c-106">**Каунтерид:** Уникальный идентификатор в базе данных, сопоставляемый с заданной текстовой строкой имени счетчика.</span><span class="sxs-lookup"><span data-stu-id="81d3c-106">**CounterID:** A unique identifier in the database that maps to a specific counter name text string.</span></span> <span data-ttu-id="81d3c-107">Это поле является первичным ключом этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="81d3c-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="81d3c-108">**MachineName:** Имя компьютера, который зарегистрировал этот набор данных.</span><span class="sxs-lookup"><span data-stu-id="81d3c-108">**MachineName:** The name of the computer that logged this data set.</span></span>
-   <span data-ttu-id="81d3c-109">**Имя_объекта:** Имя объекта производительности.</span><span class="sxs-lookup"><span data-stu-id="81d3c-109">**ObjectName:** The name of the performance object.</span></span>
-   <span data-ttu-id="81d3c-110">**CounterName:** Имя счетчика.</span><span class="sxs-lookup"><span data-stu-id="81d3c-110">**CounterName:** The name of the counter.</span></span>
-   <span data-ttu-id="81d3c-111">**CounterType:** Тип счетчика.</span><span class="sxs-lookup"><span data-stu-id="81d3c-111">**CounterType:** The counter type.</span></span> <span data-ttu-id="81d3c-112">Список типов счетчиков и их формул см. в разделе Типы счетчиков [комплекта средств для развертывания Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="81d3c-112">For a list of counter types and their formulas, see the Counter Types section of the [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span></span>
-   <span data-ttu-id="81d3c-113">**Дефаултскале:** Масштабирование по умолчанию, применяемое к необработанным данным счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="81d3c-113">**DefaultScale:** The default scaling to be applied to the raw performance counter data.</span></span>
-   <span data-ttu-id="81d3c-114">**InstanceName:** Имя экземпляра счетчика.</span><span class="sxs-lookup"><span data-stu-id="81d3c-114">**InstanceName:** The name of the counter instance.</span></span>
-   <span data-ttu-id="81d3c-115">**Инстанцеиндекс:** Номер индекса экземпляра счетчика.</span><span class="sxs-lookup"><span data-stu-id="81d3c-115">**InstanceIndex:** The index number of the counter instance.</span></span>
-   <span data-ttu-id="81d3c-116">**ParentName:** Некоторые счетчики логически связаны с другими и называются родителями.</span><span class="sxs-lookup"><span data-stu-id="81d3c-116">**ParentName:** Some counters are logically associated with others, and are referred to as parents.</span></span> <span data-ttu-id="81d3c-117">Например, родительским объектом потока является процесс, а родительский элемент драйвера логического диска — физический диск.</span><span class="sxs-lookup"><span data-stu-id="81d3c-117">For example, the parent of a thread is a process and the parent of a logical disk driver is a physical drive.</span></span> <span data-ttu-id="81d3c-118">Это поле содержит имя родителя.</span><span class="sxs-lookup"><span data-stu-id="81d3c-118">This field contains the name of the parent.</span></span> <span data-ttu-id="81d3c-119">Значение в этом поле или в поле **парентобжектид** определяет конкретный родительский экземпляр.</span><span class="sxs-lookup"><span data-stu-id="81d3c-119">Either the value in this field or the **ParentObjectID** field identifies a specific parent instance.</span></span> <span data-ttu-id="81d3c-120">Если значение в этом поле равно **null**, необходимо проверить значение в поле **парентобжектид** , чтобы указать родителя.</span><span class="sxs-lookup"><span data-stu-id="81d3c-120">If the value in this field is **NULL**, the value in the **ParentObjectID** field must be checked to identify the parent.</span></span> <span data-ttu-id="81d3c-121">Если значения в обоих полях равны **null**, то у счетчика нет родителя.</span><span class="sxs-lookup"><span data-stu-id="81d3c-121">If the values in both fields are **NULL**, the counter does not have a parent.</span></span>
-   <span data-ttu-id="81d3c-122">**Парентобжектид:** Уникальный идентификатор родителя.</span><span class="sxs-lookup"><span data-stu-id="81d3c-122">**ParentObjectID:** The unique identifier of the parent.</span></span> <span data-ttu-id="81d3c-123">Значение в этом поле или в поле **ParentName** определяет конкретный родительский экземпляр.</span><span class="sxs-lookup"><span data-stu-id="81d3c-123">The value in either this field or the **ParentName** field identifies a specific parent instance.</span></span> <span data-ttu-id="81d3c-124">Если значение в этом поле равно **null**, необходимо проверить значение в поле **ParentName** , чтобы указать родителя.</span><span class="sxs-lookup"><span data-stu-id="81d3c-124">If the value in this field is **NULL**, the value in the **ParentName** field must be checked to identify the parent.</span></span>

 

 
