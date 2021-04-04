---
description: Вы можете применить небольшое обновление к исходному административному образу MNP2000.msi, установив образец исправления MNP2000. MSP, созданный при создании пакета исправлений.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Применение пакета исправлений к административной установке
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998296"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a><span data-ttu-id="ca217-103">Применение пакета исправлений к административной установке</span><span class="sxs-lookup"><span data-stu-id="ca217-103">Applying a Patch Package to an Administrative Installation</span></span>

<span data-ttu-id="ca217-104">Вы можете применить небольшое обновление к исходному административному образу MNP2000.msi, установив образец исправления MNP2000. MSP, созданный при [создании пакета исправлений](generating-a-patch-package.md).</span><span class="sxs-lookup"><span data-stu-id="ca217-104">You may apply the small update to an administrative source image of MNP2000.msi by installing the sample patch MNP2000.msp created in [Generating a Patch Package](generating-a-patch-package.md).</span></span> <span data-ttu-id="ca217-105">Затем обновление может быть распространено для пользователей путем запроса на переустановку приложения из нового административного источника.</span><span class="sxs-lookup"><span data-stu-id="ca217-105">The update can then be propagated to users by requesting that they reinstall the application from the new administrative source image.</span></span>

<span data-ttu-id="ca217-106">Администратор может использовать следующую командную строку для обновления исходного образа, расположенного по адресу//сервер/MNP2000.msi, на новый исходный образ, который будет создан административной установкой с полностью обновленного компакт-диска.</span><span class="sxs-lookup"><span data-stu-id="ca217-106">An administrator can use the following command line to update the administrative source image located at //server/MNP2000.msi to a new source image that is the same as would be produced by an administrative installation from a fully updated CD-ROM.</span></span>

<span data-ttu-id="ca217-107">**msiexec/a//сервер/MNP2000.msi/p MNP2000. MSP**</span><span class="sxs-lookup"><span data-stu-id="ca217-107">**msiexec /a //server/MNP2000.msi /p MNP2000.msp**</span></span>

<span data-ttu-id="ca217-108">Члены Рабочей группы, использующие MNP2000, должны переустановить приложение из нового административного исходного образа, чтобы получить обновление.</span><span class="sxs-lookup"><span data-stu-id="ca217-108">Members of the workgroup using MNP2000 then must reinstall the application from the new administrative source image to receive the update.</span></span>

<span data-ttu-id="ca217-109">Чтобы полностью переустановить приложения и кэшировать обновленный MSI файл на компьютере пользователя, пользователи могут ввести одну из следующих команд.</span><span class="sxs-lookup"><span data-stu-id="ca217-109">To completely reinstall the applications and cache the updated .msi file on the user's computer, users may enter either of the following commands.</span></span>

<span data-ttu-id="ca217-110">**msiexec/фвомус//сервер/MNP2000.msi**</span><span class="sxs-lookup"><span data-stu-id="ca217-110">**msiexec /fvomus //server/MNP2000.msi**</span></span>

<span data-ttu-id="ca217-111">**msiexec/I//сервер/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="ca217-111">**msiexec /I //server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus**</span></span>

<span data-ttu-id="ca217-112">Чтобы переустановить только обновленную функцию концерта и кэшировать обновленный MSI файл на компьютере пользователя, пользователи могут ввести следующую команду.</span><span class="sxs-lookup"><span data-stu-id="ca217-112">To reinstall only the updated Concert feature and cache the updated .msi file on the user's computer, users may enter the following command.</span></span>

<span data-ttu-id="ca217-113">**msiexec/I//сервер/MNP2000.msi REINSTALL = концерт REINSTALLMODE = vomus REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="ca217-113">**msiexec /I //server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus**</span></span>

## <a name="next-example"></a><span data-ttu-id="ca217-114">Следующий пример</span><span class="sxs-lookup"><span data-stu-id="ca217-114">Next example</span></span>

[<span data-ttu-id="ca217-115">Пример локализации</span><span class="sxs-lookup"><span data-stu-id="ca217-115">A Localization Example</span></span>](a-localization-example.md)

 

 



