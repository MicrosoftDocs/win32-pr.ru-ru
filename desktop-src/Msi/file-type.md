---
description: Тип файла семантического типа является одним из типов формата ключа. Этот тип состоит из внешнего ключа в таблицу файлов, предоставленную пользователем.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Тип файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663979"
---
# <a name="file-type"></a><span data-ttu-id="b97c9-104">Тип файла</span><span class="sxs-lookup"><span data-stu-id="b97c9-104">File Type</span></span>

<span data-ttu-id="b97c9-105">Тип файла [семантического типа](semantic-types.md) является одним из [типов формата ключа](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="b97c9-105">The File Type of [semantic type](semantic-types.md) is one of the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="b97c9-106">Этот тип состоит из внешнего ключа в [таблицу файлов](file-table.md) , предоставленную пользователем.</span><span class="sxs-lookup"><span data-stu-id="b97c9-106">This type consists of a foreign key into the [File table](file-table.md) provided by the user.</span></span>

<span data-ttu-id="b97c9-107">Тип файла можно использовать со следующими видами Контекстдата.</span><span class="sxs-lookup"><span data-stu-id="b97c9-107">The File type may be used with the following kinds of ContextData.</span></span>

<span data-ttu-id="b97c9-108">**Ассембликонтекст Контекстдата**</span><span class="sxs-lookup"><span data-stu-id="b97c9-108">**AssemblyContext ContextData**</span></span>

<span data-ttu-id="b97c9-109">Этот тип можно использовать, чтобы разрешить пользователям настраивать внешние ключи для Win32 или сборок среды CLR.</span><span class="sxs-lookup"><span data-stu-id="b97c9-109">This type may be used to enable users to configure foreign keys to Win32 or common language runtime assemblies.</span></span> <span data-ttu-id="b97c9-110">Средство слияния должно подставить [идентификатор](identifier.md) установщик Windows для элементов этого типа в шаблон в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="b97c9-110">The merge tool must substitute a Windows Installer [Identifier](identifier.md) for items of this type into the template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="b97c9-111">Mergemod.dll не применяет это, а средство слияния позволяет убедиться, что пользователь предоставляет допустимый ключ в таблице File.</span><span class="sxs-lookup"><span data-stu-id="b97c9-111">Mergemod.dll does not enforce this and it is up to the merge tool to ensure that the user provides a valid key into the File table.</span></span>

<span data-ttu-id="b97c9-112">Значение null является допустимым для этого типа, если только Мсмконфигитемноннуллабле не включен в поле Attributes [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="b97c9-112">Null is a valid value for this type unless the msmConfigItemNonNullable has been included in the Attributes field of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

 

 



