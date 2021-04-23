---
description: Свойство Куалифиердескриптион только для чтения возвращает текстовую строку, описывающую квалифицированный компонент.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Свойство Installer. Куалифиердескриптион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652163"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="0eae6-103">Свойство Installer. Куалифиердескриптион</span><span class="sxs-lookup"><span data-stu-id="0eae6-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="0eae6-104">Свойство **куалифиердескриптион** только для чтения возвращает текстовую строку, описывающую квалифицированный компонент.</span><span class="sxs-lookup"><span data-stu-id="0eae6-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="0eae6-105">Эта локализуемое строка создается в столбце AppData [таблицы публишкомпонент](publishcomponent-table.md) и может отображаться для пользователя.</span><span class="sxs-lookup"><span data-stu-id="0eae6-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="0eae6-106">Квалификатор различает несколько форм одного компонента, например компонент, реализованный на нескольких языках.</span><span class="sxs-lookup"><span data-stu-id="0eae6-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="0eae6-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0eae6-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eae6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0eae6-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="0eae6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0eae6-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="0eae6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0eae6-110">Requirements</span></span>



| <span data-ttu-id="0eae6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="0eae6-111">Requirement</span></span> | <span data-ttu-id="0eae6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0eae6-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eae6-113">Версия</span><span class="sxs-lookup"><span data-stu-id="0eae6-113">Version</span></span><br/> | <span data-ttu-id="0eae6-114">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0eae6-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0eae6-115">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0eae6-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0eae6-116">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="0eae6-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0eae6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="0eae6-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="0eae6-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0eae6-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0eae6-119">IID</span><span class="sxs-lookup"><span data-stu-id="0eae6-119">IID</span></span><br/>     | <span data-ttu-id="0eae6-120">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0eae6-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="0eae6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0eae6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eae6-122">**мсиенумкомпоненткуалифиерс**</span><span class="sxs-lookup"><span data-stu-id="0eae6-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="0eae6-123">Компоненты с квалификаторами</span><span class="sxs-lookup"><span data-stu-id="0eae6-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




