---
description: Свойство Продуктлангуаже указывает язык, который должен использовать установщик для любых строк в пользовательском интерфейсе, не созданных в базе данных.
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: Продуктлангуаже, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675973"
---
# <a name="productlanguage-property"></a><span data-ttu-id="fec00-103">Продуктлангуаже, свойство</span><span class="sxs-lookup"><span data-stu-id="fec00-103">ProductLanguage property</span></span>

<span data-ttu-id="fec00-104">Свойство **продуктлангуаже** указывает язык, который должен использовать установщик для любых строк в пользовательском интерфейсе, не созданных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="fec00-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="fec00-105">Это свойство должно быть числовым идентификатором языка (LANGID).</span><span class="sxs-lookup"><span data-stu-id="fec00-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="fec00-106">Если преобразование изменяет язык пользовательского интерфейса в базе данных, оно также должно изменять значение этого свойства в соответствии с новым языком.</span><span class="sxs-lookup"><span data-stu-id="fec00-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="fec00-107">Это свойство является обязательным.</span><span class="sxs-lookup"><span data-stu-id="fec00-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec00-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fec00-108">Remarks</span></span>

<span data-ttu-id="fec00-109">Значение свойства **продуктлангуаже** должно быть одним из языков, перечисленных в свойстве [**сводки шаблона**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="fec00-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="fec00-110">При создании пакета, не зависящего от языка, задайте для свойства **продуктлангуаже** значение 0 и используйте шрифт MS Shell Dlg в качестве стиля текста для всех созданных диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="fec00-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="fec00-111">Поскольку некоторые шрифты поддерживают не все наборы символов, с помощью этого шрифта можно убедиться, что текст правильно отображается во всех локализованных версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fec00-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="fec00-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fec00-112">Requirements</span></span>



| <span data-ttu-id="fec00-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fec00-113">Requirement</span></span> | <span data-ttu-id="fec00-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fec00-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fec00-115">Версия</span><span class="sxs-lookup"><span data-stu-id="fec00-115">Version</span></span><br/> | <span data-ttu-id="fec00-116">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fec00-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fec00-117">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fec00-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fec00-118">Установщик Windows в Windows Server 2003 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fec00-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fec00-119">Сведения о минимальном пакете обновления Windows, который требуется для установщик Windows версии, см. в [установщик Windows Run-Time требования](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fec00-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fec00-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fec00-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec00-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="fec00-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




