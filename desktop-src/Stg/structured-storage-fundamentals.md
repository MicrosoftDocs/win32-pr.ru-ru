---
title: Основы структурированного хранилища
description: Структурированное хранилище предоставляет эквивалент полной файловой системы для хранения объектов.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Структурированное хранилище Стрктд STG, основы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890768"
---
# <a name="structured-storage-fundamentals"></a><span data-ttu-id="d1d46-104">Основы структурированного хранилища</span><span class="sxs-lookup"><span data-stu-id="d1d46-104">Structured Storage Fundamentals</span></span>

<span data-ttu-id="d1d46-105">Структурированное хранилище предоставляет эквивалент полной файловой системы для хранения объектов с помощью элементов, перечисленных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d1d46-105">Structured Storage provides the equivalent of a complete file system for storing objects through the elements listed in the following table.</span></span>



| <span data-ttu-id="d1d46-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="d1d46-106">Element</span></span>                                                                  | <span data-ttu-id="d1d46-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d1d46-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1d46-108">Структурированные интерфейсы хранения</span><span class="sxs-lookup"><span data-stu-id="d1d46-108">Structured Storage Interfaces</span></span>](structured-storage-interfaces.md)       | <span data-ttu-id="d1d46-109">Интерфейсы [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)и [**ирутстораже**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) вместе с набором связанных интерфейсов —[**иперсистстораже**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)и [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="d1d46-109">The [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), and [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) interfaces, along with a set of related interfaces —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), and [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> |
| [<span data-ttu-id="d1d46-110">Функции API структурированного хранилища</span><span class="sxs-lookup"><span data-stu-id="d1d46-110">Structured Storage API Functions</span></span>](structured-storage-api-functions.md) | <span data-ttu-id="d1d46-111">Вспомогательные API, которые упрощают реализацию структурированного хранилища, а также второй набор интерфейсов API для составных файлов; Это COM-реализация структурированных интерфейсов хранения.</span><span class="sxs-lookup"><span data-stu-id="d1d46-111">Helper APIs that facilitate an implementation of structured storage, as well as a second set of APIs for compound files; that is the COM implementation of the structured storage interfaces.</span></span> <span data-ttu-id="d1d46-112">COM также предоставляет набор вспомогательных структур и значений перечисления, используемых для упорядочения параметров методов интерфейса и интерфейсов API.</span><span class="sxs-lookup"><span data-stu-id="d1d46-112">COM also provides a set of supporting structures and enumeration values used to organize parameters for interface methods and APIs.</span></span>                              |
| [<span data-ttu-id="d1d46-113">Структурированные режимы доступа к хранилищу</span><span class="sxs-lookup"><span data-stu-id="d1d46-113">Structured Storage Access Modes</span></span>](structured-storage-access-modes.md)   | <span data-ttu-id="d1d46-114">Набор режимов доступа для регулирования доступа к составным файлам.</span><span class="sxs-lookup"><span data-stu-id="d1d46-114">A set of access modes for regulating access to compound files.</span></span>                                                                                                                                                                                                                                                                                                 |



 

 

 