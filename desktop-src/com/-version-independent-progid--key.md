---
title: Ключ ProgID, не зависящий от версии
description: Связывает идентификатор ProgID с идентификатором CLSID. Этот ключ используется для определения последней версии объектного приложения.
ms.assetid: fb43c8d0-d923-487f-afdf-14fc29a71e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a0bf379a06a6a05bb69a232ef91bb9fe81dc2f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488802"
---
# <a name="version-independent-progid-key"></a><span data-ttu-id="bb62c-104">Ключ ProgID, не зависящий от версии</span><span class="sxs-lookup"><span data-stu-id="bb62c-104">version-independent ProgID Key</span></span>

<span data-ttu-id="bb62c-105">Связывает идентификатор ProgID с идентификатором CLSID.</span><span class="sxs-lookup"><span data-stu-id="bb62c-105">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="bb62c-106">Этот ключ используется для определения последней версии объектного приложения.</span><span class="sxs-lookup"><span data-stu-id="bb62c-106">This key is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="bb62c-107">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="bb62c-107">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   <version-independent ProgID>
      CurVer = ProgID
```

## <a name="remarks"></a><span data-ttu-id="bb62c-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb62c-108">Remarks</span></span>

<span data-ttu-id="bb62c-109">Ключ **\_ \_ \\ \\ классов программного обеспечения файла hKey на локальном компьютере** соответствует **\_ \_ корневому ключу classes** , который был сохранен для совместимости с предыдущими версиями com.</span><span class="sxs-lookup"><span data-stu-id="bb62c-109">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key corresponds to the **HKEY\_CLASSES\_ROOT** key, which was retained for compatibility with earlier versions of COM.</span></span>

<span data-ttu-id="bb62c-110">Формат <ProgID, не *зависящий от версии* ,> <*программы*>. <*компонентов*>, разделенных точками, без пробелов и номером версии.</span><span class="sxs-lookup"><span data-stu-id="bb62c-110">The format for <*version-independent ProgID*> is <*program*>.<*component*>, separated by periods, no spaces, and no version number.</span></span> <span data-ttu-id="bb62c-111">Независимый от версии идентификатор ProgID, например ProgID, можно зарегистрировать с помощью понятного имени.</span><span class="sxs-lookup"><span data-stu-id="bb62c-111">The version-independent ProgID, like the ProgID, can be registered with a human-readable name.</span></span>

<span data-ttu-id="bb62c-112">*ProgID* — это ProgID последней установленной версии класса.</span><span class="sxs-lookup"><span data-stu-id="bb62c-112">*ProgID* is the ProgID of the latest installed version of the class.</span></span>

<span data-ttu-id="bb62c-113">Приложения должны зарегистрировать программный идентификатор, не зависящий от версии, в ключе ProgID, не *зависящем от версии* .</span><span class="sxs-lookup"><span data-stu-id="bb62c-113">Applications must register a version-independent programmatic identifier under the *version-independent ProgID* key.</span></span> <span data-ttu-id="bb62c-114">Идентификатор ProgID, не зависящий от версии, относится к классу приложения и не меняется с версии на версию, вместо этого остается постоянной для всех версионсâ €, например документа Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="bb62c-114">The version-independent ProgID refers to the application's class and does not change from version to version, instead remaining constant across all versionsâ€”for example, Microsoft Word Document.</span></span> <span data-ttu-id="bb62c-115">Он используется с языками макросов и ссылается на текущую установленную версию класса приложения.</span><span class="sxs-lookup"><span data-stu-id="bb62c-115">It is used with macro languages and refers to the currently installed version of the application's class.</span></span> <span data-ttu-id="bb62c-116">Идентификатор ProgID, не зависящий от версии, должен соответствовать имени последней версии приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="bb62c-116">The version-independent ProgID must correspond to the name of the latest version of the object application.</span></span>

<span data-ttu-id="bb62c-117">Например, идентификатор ProgID, не зависящий от версии, используется, когда приложение-контейнер создает диаграмму или таблицу с кнопкой на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bb62c-117">For example, the version-independent ProgID is used when a container application creates a chart or table with a toolbar button.</span></span> <span data-ttu-id="bb62c-118">В этом случае приложение может использовать идентификатор ProgID, не зависящий от версии, для определения последней версии необходимого объектного приложения.</span><span class="sxs-lookup"><span data-stu-id="bb62c-118">In this situation, the application can use the version-independent ProgID to determine the latest version of the needed object application.</span></span>

<span data-ttu-id="bb62c-119">Идентификатор ProgID, не зависящий от версии, хранится и обслуживается исключительно кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="bb62c-119">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="bb62c-120">При задании идентификатора ProgID, не зависящего от версии, функция [**клсидфромпрогид**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) возвращает идентификатор CLSID текущей версии.</span><span class="sxs-lookup"><span data-stu-id="bb62c-120">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="bb62c-121">Для преобразования между этими двумя представлениями можно использовать [**клсидфромпрогид**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) и [**прогидфромклсид**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="bb62c-121">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

<span data-ttu-id="bb62c-122">Чтобы изменить идентификатор на отображаемую строку, можно использовать [**иолеобжект:: жетусертипе**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) или [**олерегжетусертипе**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) .</span><span class="sxs-lookup"><span data-stu-id="bb62c-122">You can use [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) or [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype) to change the identifier to a displayable string.</span></span>

<span data-ttu-id="bb62c-123">Если пользовательский обработчик не используется, для записи следует задать значение OLE32.DLL, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="bb62c-123">If a custom handler is not used, the entry should be set to OLE32.DLL, as shown in the following example:</span></span>

```
HKEY_CLASSES_ROOT\CLSID\{00000402-0000-0000-C000-000000000046}
   InprocHandler = ole32.dll
```

## <a name="related-topics"></a><span data-ttu-id="bb62c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="bb62c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb62c-125">**клсидфромпрогид**</span><span class="sxs-lookup"><span data-stu-id="bb62c-125">**CLSIDFromProgID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid)
</dt> <dt>

[<span data-ttu-id="bb62c-126">**прогидфромклсид**</span><span class="sxs-lookup"><span data-stu-id="bb62c-126">**ProgIDFromCLSID**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid)
</dt> <dt>

[<span data-ttu-id="bb62c-127"><ProgID> Раздел</span><span class="sxs-lookup"><span data-stu-id="bb62c-127"><ProgID> Key</span></span>](-progid--key.md)
</dt> </dl>

 

 




