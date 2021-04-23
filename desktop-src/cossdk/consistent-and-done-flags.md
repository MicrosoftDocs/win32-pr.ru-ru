---
description: Флаги consistent и Done
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Флаги consistent и Done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539431"
---
# <a name="consistent-and-done-flags"></a><span data-ttu-id="a8ecc-103">Флаги consistent и Done</span><span class="sxs-lookup"><span data-stu-id="a8ecc-103">Consistent and Done Flags</span></span>

<span data-ttu-id="a8ecc-104">COM+ всегда создает объект контекста перед активацией транзакционного объекта.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-104">COM+ always creates a context object before activating a transactional object.</span></span> <span data-ttu-id="a8ecc-105">Объект контекста содержит сведения, относящиеся к объекту, такие как его создатель и идентификатор транзакции.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-105">The context object holds object-related information, such as its creator and its transaction identifier.</span></span> <span data-ttu-id="a8ecc-106">Каждый объект контекста также содержит *последовательный флаг* и *флаг Done*.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-106">Each context object also contains a *consistent flag* and a *done flag*.</span></span> <span data-ttu-id="a8ecc-107">Вместе эти флаги определяют состояние транзакционного объекта.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-107">Together these flags determine the status of the transactional object.</span></span>

<span data-ttu-id="a8ecc-108">Флаг consistent указывает, что транзакционный объект является согласованным или несогласованным.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-108">The consistent flag indicates that the transactional object is either consistent or inconsistent.</span></span> <span data-ttu-id="a8ecc-109">Конкретные сведения о том, что делает целостность состояния объекта, зависит от программиста.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-109">The specific details of what makes an object's state consistent is up to the programmer.</span></span> <span data-ttu-id="a8ecc-110">Когда вызов метода устанавливает для этого флага значение true, объект является последовательным.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-110">When a method call sets this flag to True, the object is consistent.</span></span> <span data-ttu-id="a8ecc-111">Значение false указывает, что объект не согласуется.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-111">False indicates that the object is inconsistent.</span></span> <span data-ttu-id="a8ecc-112">COM+ устанавливает для флага значение true при создании экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-112">COM+ sets the flag to True when it creates an object instance.</span></span> <span data-ttu-id="a8ecc-113">Последовательный объект готов к продолжению транзакции.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-113">A consistent object is ready to proceed with the transaction.</span></span> <span data-ttu-id="a8ecc-114">Пока объект остается активным, последующие вызовы метода могут многократно переключить флаг consistent с true на false и наоборот.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-114">While an object remains active, subsequent method calls can repeatedly switch the consistent flag from True to False and vice versa.</span></span>

<span data-ttu-id="a8ecc-115">Флаг Done определяет длительность транзакции.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-115">The done flag determines the duration of a transaction.</span></span> <span data-ttu-id="a8ecc-116">При возврате вызова метода COM+ проверяет флаг Done.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-116">When a method call returns, COM+ inspects the done flag.</span></span> <span data-ttu-id="a8ecc-117">Если метод устанавливает для этого флага значение true, COM+ деактивирует объект и заметит флаг consistent.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-117">If the method sets this flag to True, COM+ deactivates the object and notes the consistent flag.</span></span> <span data-ttu-id="a8ecc-118">Если флаг done имеет значение false, то COM+ не активирует объект или замещает флаг consistent.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-118">When the done flag is False, COM+ neither deactivates the object nor notes the consistent flag.</span></span> <span data-ttu-id="a8ecc-119">COM+ задает для флага done значение false при создании экземпляра объекта.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-119">COM+ sets the done flag to False when it creates an object instance.</span></span>

<span data-ttu-id="a8ecc-120">Флаг consistent приводит голосование к фиксации или прерыванию транзакции, в которой она выполняется, а флаг done завершает голосование.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-120">The consistent flag casts a vote to commit or abort the transaction in which it executes, and the done flag finalizes the vote.</span></span> <span data-ttu-id="a8ecc-121">COM+ проверяет флаг consistent, когда флаг Done установлен в значение true для возвращаемого вызова метода или когда объект деактивируется.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-121">COM+ inspects the consistent flag when the done flag is set to True on a method call return or when the object deactivates.</span></span> <span data-ttu-id="a8ecc-122">Несмотря на то что последовательный флаг объекта может постоянно меняться в каждом вызове метода, учитываются только последние изменения.</span><span class="sxs-lookup"><span data-stu-id="a8ecc-122">Although an object's consistent flag can change repeatedly within each method call, only the last change counts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8ecc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a8ecc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8ecc-124">Управление автоматическими транзакциями в COM+</span><span class="sxs-lookup"><span data-stu-id="a8ecc-124">Managing Automatic Transactions in COM+</span></span>](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[<span data-ttu-id="a8ecc-125">Установка флагов consistent и Done</span><span class="sxs-lookup"><span data-stu-id="a8ecc-125">Setting the Consistent and Done Flags</span></span>](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



