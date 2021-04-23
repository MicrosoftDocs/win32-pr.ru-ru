---
description: Можно использовать установщик Windows для обнаружения отсутствующих компонентов или файлов, а затем переустановить компоненты, содержащие отсутствующие компоненты.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Установка отсутствующего компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650696"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="a1029-103">Установка отсутствующего компонента</span><span class="sxs-lookup"><span data-stu-id="a1029-103">Installing a Missing Component</span></span>

<span data-ttu-id="a1029-104">Можно использовать установщик Windows для обнаружения отсутствующих компонентов или файлов, а затем переустановить компоненты, содержащие отсутствующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="a1029-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="a1029-105">Поскольку установщик устанавливает компоненты, а не компоненты, сначала необходимо разрешить компоненту, к которому принадлежит отсутствующий файл, а затем установить компонент, содержащий этот компонент.</span><span class="sxs-lookup"><span data-stu-id="a1029-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="a1029-106">Если с компонентом связана несколько компонентов, установщик устанавливает компонент, требующий наименьшего места на диске.</span><span class="sxs-lookup"><span data-stu-id="a1029-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="a1029-107">При вызове [**мсижеткомпонентпас**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)можно проверить наличие файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="a1029-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="a1029-108">Однако по-прежнему могут отсутствовать другие файлы, принадлежащие компоненту.</span><span class="sxs-lookup"><span data-stu-id="a1029-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="a1029-109">В этом сценарии вызовите [**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="a1029-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="a1029-110">Затем установщик разрешается в тот компонент, которому принадлежит файл, и устанавливает компонент, связанный с компонентом, для которого требуется наименьшее место на диске.</span><span class="sxs-lookup"><span data-stu-id="a1029-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="a1029-111">Если функция [**мсижеткомпонентпас**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) неожиданно завершается сбоем, необходимо установить все отсутствующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="a1029-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="a1029-112">В следующей процедуре показано, как установить недостающие компоненты.</span><span class="sxs-lookup"><span data-stu-id="a1029-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="a1029-113">**Обнаружение и установка отсутствующего компонента**</span><span class="sxs-lookup"><span data-stu-id="a1029-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="a1029-114">Вызовите [**мсижеткомпонентпас**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) , чтобы убедиться в наличии файла ключа компонента.</span><span class="sxs-lookup"><span data-stu-id="a1029-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="a1029-115">Однако даже если файл ключа компонента существует, все равно возможно, что отсутствуют другие файлы, принадлежащие компоненту.</span><span class="sxs-lookup"><span data-stu-id="a1029-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="a1029-116">Если компонент, связанный с компонентом, неизвестен, вызовите функцию [**мсиинсталлмиссингкомпонент**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) .</span><span class="sxs-lookup"><span data-stu-id="a1029-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="a1029-117">Если функция, связанная с компонентом, известна, вызовите функцию [**мсиконфигурефеатуре**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) или [**мсипровидекомпонент**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) .</span><span class="sxs-lookup"><span data-stu-id="a1029-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="a1029-118">Вызовите [**мсиинсталлмиссингфиле**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) , если приложению не удается открыть файл.</span><span class="sxs-lookup"><span data-stu-id="a1029-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



