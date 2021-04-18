---
title: DataFormats
description: Указывает форматы данных по умолчанию и основные параметры, поддерживаемые приложением.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Формат COM раздела реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700697"
---
# <a name="dataformats"></a><span data-ttu-id="39359-104">DataFormats</span><span class="sxs-lookup"><span data-stu-id="39359-104">DataFormats</span></span>

<span data-ttu-id="39359-105">Указывает форматы данных по умолчанию и основные параметры, поддерживаемые приложением.</span><span class="sxs-lookup"><span data-stu-id="39359-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="39359-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="39359-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="39359-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39359-107">Remarks</span></span>

<span data-ttu-id="39359-108">Значение *File/Format* указывает основной файл или формат объекта по умолчанию для объектов этого класса.</span><span class="sxs-lookup"><span data-stu-id="39359-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="39359-109">Значение *formats* указывает список форматов для реализаций по умолчанию [**енумформатетк**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), где *n* — целочисленный индекс, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="39359-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="39359-110">Например, *n*  =  *Format*, *аспект*, *средний*, *флаг*, где *Формат* — формат буфера обмена, *аспект* — один или несколько членов [**дваспект**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *средний* — один или несколько членов [**тимед**](/windows/win32/api/objidl/ne-objidl-tymed), а *флаг* — один или несколько элементов [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span><span class="sxs-lookup"><span data-stu-id="39359-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="39359-111">См. также</span><span class="sxs-lookup"><span data-stu-id="39359-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39359-112">**IDataObject:: Енумформатетк**</span><span class="sxs-lookup"><span data-stu-id="39359-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="39359-113">**IDataObject:: GetData**</span><span class="sxs-lookup"><span data-stu-id="39359-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="39359-114">**IDataObject:: SetData**</span><span class="sxs-lookup"><span data-stu-id="39359-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




