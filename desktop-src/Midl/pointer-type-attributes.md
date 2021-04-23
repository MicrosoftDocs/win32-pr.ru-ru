---
title: Атрибуты типа указателя
description: Следующие атрибуты определяют характеристики указателей.
ms.assetid: 310d0dfe-eef3-447e-89fb-40f620976d00
keywords:
- IDL-MIDL, атрибуты, тип указателя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71371fff80d541242fcdc41d6c8adcc93dcdb754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779892"
---
# <a name="pointer-type-attributes"></a><span data-ttu-id="f1601-104">Атрибуты типа указателя</span><span class="sxs-lookup"><span data-stu-id="f1601-104">Pointer Type Attributes</span></span>

<span data-ttu-id="f1601-105">Следующие атрибуты определяют характеристики указателей.</span><span class="sxs-lookup"><span data-stu-id="f1601-105">The following attributes specify the characteristics of pointers.</span></span>



| <span data-ttu-id="f1601-106">attribute</span><span class="sxs-lookup"><span data-stu-id="f1601-106">Attribute</span></span>                                   | <span data-ttu-id="f1601-107">Использование</span><span class="sxs-lookup"><span data-stu-id="f1601-107">Usage</span></span>                                                                                                                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1601-108">**ptr**</span><span class="sxs-lookup"><span data-stu-id="f1601-108">**ptr**</span></span>](ptr.md)                          | <span data-ttu-id="f1601-109">Назначает указатель как полный указатель со всеми возможностями указателя языка C, включая псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="f1601-109">Designates a pointer as a full pointer, with all the capabilities of a C-language pointer, including aliasing.</span></span>                                                                                       |
| [<span data-ttu-id="f1601-110">**ref**</span><span class="sxs-lookup"><span data-stu-id="f1601-110">**ref**</span></span>](ref.md)                          | <span data-ttu-id="f1601-111">Обозначает простейший тип указателя в MIDL — один, который просто предоставляет адрес некоторых данных.</span><span class="sxs-lookup"><span data-stu-id="f1601-111">Designates the simplest type of pointer in MIDL—one that simply provides the address of some data.</span></span> <span data-ttu-id="f1601-112">Ссылочные указатели никогда не могут иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="f1601-112">Reference pointers can never be null.</span></span>                                                             |
| [<span data-ttu-id="f1601-113">**однозначно**</span><span class="sxs-lookup"><span data-stu-id="f1601-113">**unique**</span></span>](unique.md)                    | <span data-ttu-id="f1601-114">Позволяет указателю иметь значение null, но не поддерживает псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="f1601-114">Lets a pointer be null, but does not support aliasing.</span></span>                                                                                                                                               |
| [<span data-ttu-id="f1601-115">**Указатель \_ по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="f1601-115">**pointer\_default**</span></span>](pointer-default.md) | <span data-ttu-id="f1601-116">Применяется к интерфейсу для указания типа указателя по умолчанию для всех указателей в этом интерфейсе, за исключением указателей на параметры верхнего уровня, которые по умолчанию автоматически задаются как [**Ссылочные**](ref.md) указатели.</span><span class="sxs-lookup"><span data-stu-id="f1601-116">Applied to an interface to specify the default pointer type for all pointers in that interface, except for top-level parameter pointers, which automatically default to [**ref**](ref.md) pointers.</span></span> |
| [<span data-ttu-id="f1601-117">**IID \_ —**</span><span class="sxs-lookup"><span data-stu-id="f1601-117">**iid\_is**</span></span>](iid-is.md)                   | <span data-ttu-id="f1601-118">Предоставляет идентификатор интерфейса COM, который является объектом указателя.</span><span class="sxs-lookup"><span data-stu-id="f1601-118">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                                                                                            |
| [<span data-ttu-id="f1601-119">**Строка**</span><span class="sxs-lookup"><span data-stu-id="f1601-119">**string**</span></span>](string.md)                    | <span data-ttu-id="f1601-120">Указывает, что указатель указывает на строку.</span><span class="sxs-lookup"><span data-stu-id="f1601-120">Specifies that the pointer points to a string.</span></span>                                                                                                                                                       |



 

 

 




