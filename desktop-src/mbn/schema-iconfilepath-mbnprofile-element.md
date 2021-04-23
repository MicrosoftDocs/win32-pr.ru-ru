---
description: Содержит путь к файлу значка для соединения.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Иконфилепас (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711163"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="62864-103">Иконфилепас (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="62864-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="62864-104">Элемент **иконфилепас (мбнпрофиле)** содержит путь к файлу значка для соединения.</span><span class="sxs-lookup"><span data-stu-id="62864-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="62864-105">В пользовательском интерфейсе подключения операционной системы будет отображаться этот значок, когда соединение устанавливается с помощью этого элемента.</span><span class="sxs-lookup"><span data-stu-id="62864-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="62864-106">При передаче XML для создания профиля в методе [**креатеконнектионпрофиле**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) интерфейса [**имбнконнектионпрофилеманажер**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) этот путь должен указывать на исходное расположение файла значка.</span><span class="sxs-lookup"><span data-stu-id="62864-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="62864-107">При успешном создании объекта [**имбнконнектионпрофиле**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) служба мобильной широкополосной связи скопирует файл значка в внутреннее хранилище, а путь к профилю будет изменен в соответствии с этим.</span><span class="sxs-lookup"><span data-stu-id="62864-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="62864-108">Файл значка должен иметь формат. bmp с размером 32X32 пикселя.</span><span class="sxs-lookup"><span data-stu-id="62864-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="62864-109">Этот элемент представляет собой строку длиной до 1024 символов, содержащую абсолютный путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="62864-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="62864-110">Элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="62864-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="62864-111">Элемент **иконфилепас** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="62864-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="62864-112">Требования</span><span class="sxs-lookup"><span data-stu-id="62864-112">Requirements</span></span>



| <span data-ttu-id="62864-113">Требование</span><span class="sxs-lookup"><span data-stu-id="62864-113">Requirement</span></span> | <span data-ttu-id="62864-114">Значение</span><span class="sxs-lookup"><span data-stu-id="62864-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="62864-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="62864-115">Minimum supported client</span></span><br/> | <span data-ttu-id="62864-116">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="62864-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="62864-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="62864-117">Minimum supported server</span></span><br/> | <span data-ttu-id="62864-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="62864-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="62864-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="62864-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="62864-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="62864-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="62864-121">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="62864-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="62864-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="62864-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="62864-123">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="62864-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




