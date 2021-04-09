---
title: Ключ ProgID
description: Программный идентификатор (ProgID) — это запись реестра, которая может быть связана с идентификатором CLSID. Как и CLSID, идентификатор ProgID определяет класс, но с меньшей точностью, поскольку он не обязательно должен быть глобально уникальным.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070990"
---
# <a name="progid-key"></a><span data-ttu-id="d2ea2-104">Ключ ProgID</span><span class="sxs-lookup"><span data-stu-id="d2ea2-104">ProgID Key</span></span>

<span data-ttu-id="d2ea2-105">Программный идентификатор (ProgID) — это запись реестра, которая может быть связана с идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-105">A programmatic identifier (ProgID) is a registry entry that can be associated with a CLSID.</span></span> <span data-ttu-id="d2ea2-106">Как и CLSID, идентификатор ProgID определяет класс, но с меньшей точностью, поскольку он не обязательно должен быть глобально уникальным.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-106">Like the CLSID, the ProgID identifies a class but with less precision because it is not guaranteed to be globally unique.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d2ea2-107">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="d2ea2-107">Registry Entry</span></span>

<span data-ttu-id="d2ea2-108">**HKey \_ \_ \\ \\ Классы программного обеспечения локального компьютера** \\ *{* ProgID *}*</span><span class="sxs-lookup"><span data-stu-id="d2ea2-108">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**\\ *{* ProgID *}*</span></span>



| <span data-ttu-id="d2ea2-109">Раздел реестра</span><span class="sxs-lookup"><span data-stu-id="d2ea2-109">Registry key</span></span>                            | <span data-ttu-id="d2ea2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d2ea2-110">Description</span></span>                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d2ea2-111">**ЭТОМУ**</span><span class="sxs-lookup"><span data-stu-id="d2ea2-111">**CLSID**</span></span>](clsid.md)                  | <span data-ttu-id="d2ea2-112">Связывает идентификатор ProgID с идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-112">Associates a ProgID with a CLSID.</span></span>                                  |
| [<span data-ttu-id="d2ea2-113">**Insertable**</span><span class="sxs-lookup"><span data-stu-id="d2ea2-113">**Insertable**</span></span>](insertable-progid.md) | <span data-ttu-id="d2ea2-114">Указывает, что этот класс может быть вставлен в контейнеры OLE 2.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-114">Indicates that this class is insertable in OLE 2 containers.</span></span>       |
| [<span data-ttu-id="d2ea2-115">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="d2ea2-115">**Protocol**</span></span>](protocol.md)            | <span data-ttu-id="d2ea2-116">Указывает, что этот класс OLE 2 может быть вставлен в контейнеры OLE 1.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-116">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span> |
| [<span data-ttu-id="d2ea2-117">**Shell**</span><span class="sxs-lookup"><span data-stu-id="d2ea2-117">**Shell**</span></span>](shell.md)                  | <span data-ttu-id="d2ea2-118">Предоставляет данные для печати оболочки Windows 3,1 и **открытия файлов** .</span><span class="sxs-lookup"><span data-stu-id="d2ea2-118">Provides Windows 3.1 shell printing and **File Open** information.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d2ea2-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d2ea2-119">Remarks</span></span>

<span data-ttu-id="d2ea2-120">Идентификатор ProgID можно использовать в ситуациях программирования, когда невозможно использовать CLSID.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-120">You can use a ProgID in programming situations where it is not possible to use a CLSID.</span></span> <span data-ttu-id="d2ea2-121">Идентификаторы ProgID не должны присутствовать в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-121">ProgIDs should not appear in the user interface.</span></span> <span data-ttu-id="d2ea2-122">Идентификаторы ProgID не обязательно должны быть уникальными, поэтому их можно использовать только в том случае, если конфликты имен являются управляемыми.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-122">ProgIDs are not guaranteed to be unique, so they can be used only where name collisions are manageable.</span></span>

<span data-ttu-id="d2ea2-123">Формат ProgID — <*программа*>. <*компонент*>. <*версии*>, разделенные точками и без пробелов, как в Word.Docумент. 6.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-123">The format of a ProgID is <*Program*>.<*Component*>.<*Version*>, separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="d2ea2-124">Идентификатор ProgID должен соответствовать следующим требованиям:</span><span class="sxs-lookup"><span data-stu-id="d2ea2-124">The ProgID must comply with the following requirements:</span></span>

-   <span data-ttu-id="d2ea2-125">Не более 39 символов.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-125">Have no more than 39 characters.</span></span>
-   <span data-ttu-id="d2ea2-126">Не должны содержать знаки препинания (включая символы подчеркивания), за исключением одного или нескольких периодов.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-126">Contain no punctuation (including underscores) except one or more periods.</span></span>
-   <span data-ttu-id="d2ea2-127">Не начинается с цифры.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-127">Not start with a digit.</span></span>
-   <span data-ttu-id="d2ea2-128">Отличаться от имени класса любого приложения OLE 1, включая версию OLE 1 приложения, если таковая имеется.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-128">Be different from the class name of any OLE 1 application, including the OLE 1 version of the same application, if there is one.</span></span>

<span data-ttu-id="d2ea2-129">Так как ProgID не должен отображаться в пользовательском интерфейсе, можно получить отображаемое имя, вызвав [**иолеобжект:: жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span><span class="sxs-lookup"><span data-stu-id="d2ea2-129">Because the ProgID should not appear in the user interface, you can obtain a displayable name by calling [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype).</span></span> <span data-ttu-id="d2ea2-130">См. также раздел [**олерегжетусертипе**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span><span class="sxs-lookup"><span data-stu-id="d2ea2-130">Also, see [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).</span></span>

<span data-ttu-id="d2ea2-131">Ключ **\_ \_ \\ \\ классов программного обеспечения файла hKey на локальном компьютере** соответствует **\_ \_ корневому ключу classes** , который был сохранен для совместимости с предыдущими версиями com.</span><span class="sxs-lookup"><span data-stu-id="d2ea2-131">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2ea2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="d2ea2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ea2-133">**Иолеобжект:: Жетусертипе**</span><span class="sxs-lookup"><span data-stu-id="d2ea2-133">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[<span data-ttu-id="d2ea2-134">**олерегжетусертипе**</span><span class="sxs-lookup"><span data-stu-id="d2ea2-134">**OleRegGetUserType**</span></span>](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




