---
description: Регистрирует компьютер в иерархии сертификатов с помощью шаблона, отображаемого имени сертификата и описания сертификата.
ms.assetid: d9e01767-f6e8-4fd6-a848-8d5acf57407e
title: енроллсимплемачинецерт
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8582bc73fdee7e8be6b2cff8d0aec81b84487307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683665"
---
# <a name="enrollsimplemachinecert"></a><span data-ttu-id="f37cf-103">енроллсимплемачинецерт</span><span class="sxs-lookup"><span data-stu-id="f37cf-103">enrollSimpleMachineCert</span></span>

<span data-ttu-id="f37cf-104">Пример Енроллсимплемачинецерт регистрирует компьютер в иерархии сертификатов с помощью шаблона, отображаемого имени сертификата и описания сертификата.</span><span class="sxs-lookup"><span data-stu-id="f37cf-104">The enrollSimpleMachineCert sample enrolls a computer in a certificate hierarchy by using a template, a certificate display name, and the certificate description.</span></span>

## <a name="location"></a><span data-ttu-id="f37cf-105">Расположение</span><span class="sxs-lookup"><span data-stu-id="f37cf-105">Location</span></span>

<span data-ttu-id="f37cf-106">При установке пакета средств разработки программного обеспечения (SDK) для Microsoft Windows устанавливается версия C++ образца по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security SSL \\ Certificate \\ \\ енроллсимплемачинецерт.</span><span class="sxs-lookup"><span data-stu-id="f37cf-106">When you install the Microsoft Windows Software Development Kit (SDK), a C++ version of the sample is installed, by default, in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VC\\EnrollSimpleMachineCert folder.</span></span> <span data-ttu-id="f37cf-107">Версия VBScript установлена в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 Certificate \\ \\ енроллсимплемачинецерт vbs.</span><span class="sxs-lookup"><span data-stu-id="f37cf-107">A VBScript version is installed in the *%ProgramFiles%*\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Security\\X509 Certificate Enrollment\\VBS\\EnrollSimpleMachineCert folder.</span></span>

## <a name="discussion"></a><span data-ttu-id="f37cf-108">Разговор</span><span class="sxs-lookup"><span data-stu-id="f37cf-108">Discussion</span></span>

<span data-ttu-id="f37cf-109">Пример Енроллсимплемачинецерт:</span><span class="sxs-lookup"><span data-stu-id="f37cf-109">The enrollSimpleMachineCert sample:</span></span>

1.  <span data-ttu-id="f37cf-110">Обрабатывает аргументы командной строки.</span><span class="sxs-lookup"><span data-stu-id="f37cf-110">Processes the command line arguments.</span></span> <span data-ttu-id="f37cf-111">Командная строка должна содержать имя шаблона, отображаемое имя сертификата и описание сертификата.</span><span class="sxs-lookup"><span data-stu-id="f37cf-111">The command line should contain the name of the template, a certificate display name, and a certificate description.</span></span>
2.  <span data-ttu-id="f37cf-112">Создает объект [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) и инициализирует его с помощью шаблона, указанного в командной строке.</span><span class="sxs-lookup"><span data-stu-id="f37cf-112">Creates an [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) object and initializes it by using the template specified on the command line.</span></span> <span data-ttu-id="f37cf-113">Значение Контекстадминистраторфорцемачине для первого параметра указывает, что сертификат запрашивается администратором, действующим от имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="f37cf-113">The ContextAdministratorForceMachine value for the first parameter specifies that the certificate is being requested by an administrator acting on behalf of a computer.</span></span>
3.  <span data-ttu-id="f37cf-114">Добавляет отображаемое имя и описание в объект регистрации.</span><span class="sxs-lookup"><span data-stu-id="f37cf-114">Adds the display name and description to the enrollment object.</span></span>
4.  <span data-ttu-id="f37cf-115">Пытается зарегистрировать запрос сертификата и проверяет состояние процесса.</span><span class="sxs-lookup"><span data-stu-id="f37cf-115">Attempts to enroll the certificate request and checks the status of the process.</span></span> <span data-ttu-id="f37cf-116">Функция Чеккенроллстатус определена в Енроллкоммон. cpp.</span><span class="sxs-lookup"><span data-stu-id="f37cf-116">The checkEnrollStatus function is defined in enrollCommon.cpp.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f37cf-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f37cf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f37cf-118">Использование прилагаемых примеров</span><span class="sxs-lookup"><span data-stu-id="f37cf-118">Using the Included Samples</span></span>](using-the-included-samples.md)
</dt> </dl>

 

 



