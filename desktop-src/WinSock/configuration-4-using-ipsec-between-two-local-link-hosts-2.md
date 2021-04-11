---
description: Эта конфигурация создает сопоставление безопасности (SA) IPsec между двумя узлами в одной подсети для выполнения проверки подлинности с помощью заголовка проверки подлинности (AH) и алгоритма хэширования Message Digest 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: Конфигурация 3. использование IPsec между двумя узлами локальной связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145100"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a><span data-ttu-id="246f8-103">Конфигурация 3. использование IPsec между двумя узлами локальной связи</span><span class="sxs-lookup"><span data-stu-id="246f8-103">Configuration 3: Using IPsec Between Two Local-link Hosts</span></span>

<span data-ttu-id="246f8-104">Эта конфигурация создает сопоставление безопасности (SA) IPsec между двумя узлами в одной подсети для выполнения проверки подлинности с помощью заголовка проверки подлинности (AH) и алгоритма хэширования Message Digest 5 (MD5).</span><span class="sxs-lookup"><span data-stu-id="246f8-104">This configuration creates an IPsec Security Association (SA) between two hosts on the same subnet to perform authentication using the Authentication Header (AH) and the Message Digest 5 (MD5) hashing algorithm.</span></span> <span data-ttu-id="246f8-105">В этом примере показанная конфигурация защищает весь трафик между двумя соседними узлами: узел 1 с адресом локальной ссылки FE80:: 2AA: FF: FE53: A92C и узлом 2 с адресом локальной ссылки FE80:: 2AA: FF: FE92: D0F1.</span><span class="sxs-lookup"><span data-stu-id="246f8-105">In this example, the configuration shown secures all traffic between two neighboring hosts: Host 1, with the link-local address FE80::2AA:FF:FE53:A92C, and Host 2, with the link-local address FE80::2AA:FF:FE92:D0F1.</span></span>

<span data-ttu-id="246f8-106">**Использование IPsec между двумя узлами локальной связи**</span><span class="sxs-lookup"><span data-stu-id="246f8-106">**To use IPsec between two local-link hosts**</span></span>

1.  <span data-ttu-id="246f8-107">На узле 1 Создайте пустые файлы сопоставления безопасности (SAD) и политики безопасности (SPD) с помощью команды ipsec6 c.</span><span class="sxs-lookup"><span data-stu-id="246f8-107">On Host 1, create blank security association (SAD) and security policy (SPD) files by using the ipsec6 c command.</span></span> <span data-ttu-id="246f8-108">В этом примере команда Ipsec6.exe ipsec6 Test c.</span><span class="sxs-lookup"><span data-stu-id="246f8-108">In this example, the Ipsec6.exe command is ipsec6 c test.</span></span> <span data-ttu-id="246f8-109">При этом создаются два файла для ручной настройки сопоставлений безопасности (Test. sad) и политик безопасности (Test. SPD).</span><span class="sxs-lookup"><span data-stu-id="246f8-109">This creates two files to manually configure security associations (Test.sad) and security policies (Test.spd).</span></span>
2.  <span data-ttu-id="246f8-110">На узле 1 измените файл SPD, добавив политику безопасности, которая защищает весь трафик между узлом 1 и узлом 2.</span><span class="sxs-lookup"><span data-stu-id="246f8-110">On Host 1, edit the SPD file to add a security policy that secures all traffic between Host 1 and Host 2.</span></span>

    <span data-ttu-id="246f8-111">В следующей таблице показана политика безопасности, добавленная в файл Test. SPD перед первой записью в этом примере (первая запись в файле Test. SPD не была изменена).</span><span class="sxs-lookup"><span data-stu-id="246f8-111">The following table shows the security policy added to the Test.spd file before the first entry for this example (the first entry in the Test.spd file was not modified).</span></span>

    | <span data-ttu-id="246f8-112">Имя поля в файле SPD</span><span class="sxs-lookup"><span data-stu-id="246f8-112">SPD file field name</span></span> | <span data-ttu-id="246f8-113">Пример значения</span><span class="sxs-lookup"><span data-stu-id="246f8-113">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="246f8-114">**Политика**</span><span class="sxs-lookup"><span data-stu-id="246f8-114">**Policy**</span></span>          | <span data-ttu-id="246f8-115">2</span><span class="sxs-lookup"><span data-stu-id="246f8-115">2</span></span>                          |
    | <span data-ttu-id="246f8-116">**ремотеипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-116">**RemoteIPAddr**</span></span>    | <span data-ttu-id="246f8-117">**FE80:: 2AA: FF: FE92: D0F1**</span><span class="sxs-lookup"><span data-stu-id="246f8-117">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="246f8-118">**локалипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-118">**LocalIPAddr**</span></span>     | \*                         |
    | <span data-ttu-id="246f8-119">**ремотепорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-119">**RemotePort**</span></span>      | \*                         |
    | <span data-ttu-id="246f8-120">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-120">**Protocol**</span></span>        | \*                         |
    | <span data-ttu-id="246f8-121">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="246f8-121">**LocalPort**</span></span>       | \*                         |
    | <span data-ttu-id="246f8-122">**ипсекпротокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-122">**IPSecProtocol**</span></span>   | <span data-ttu-id="246f8-123">**ЗАГОЛОВКИ**</span><span class="sxs-lookup"><span data-stu-id="246f8-123">**AH**</span></span>                     |
    | <span data-ttu-id="246f8-124">**ипсекмоде**</span><span class="sxs-lookup"><span data-stu-id="246f8-124">**IPSecMode**</span></span>       | <span data-ttu-id="246f8-125">**ПЕРЕМЕЩЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="246f8-125">**TRANSPORT**</span></span>              |
    | <span data-ttu-id="246f8-126">**ремотегвипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-126">**RemoteGWIPAddr**</span></span>  | \*                         |
    | <span data-ttu-id="246f8-127">**сабундлеиндекс**</span><span class="sxs-lookup"><span data-stu-id="246f8-127">**SABundleIndex**</span></span>   | <span data-ttu-id="246f8-128">**NONE**</span><span class="sxs-lookup"><span data-stu-id="246f8-128">**NONE**</span></span>                   |
    | <span data-ttu-id="246f8-129">**Направление**</span><span class="sxs-lookup"><span data-stu-id="246f8-129">**Direction**</span></span>       | <span data-ttu-id="246f8-130">**бидирект**</span><span class="sxs-lookup"><span data-stu-id="246f8-130">**BIDIRECT**</span></span>               |
    | <span data-ttu-id="246f8-131">**Действие**</span><span class="sxs-lookup"><span data-stu-id="246f8-131">**Action**</span></span>          | <span data-ttu-id="246f8-132">**КАСАТЬСЯ**</span><span class="sxs-lookup"><span data-stu-id="246f8-132">**APPLY**</span></span>                  |
    | <span data-ttu-id="246f8-133">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="246f8-133">**InterfaceIndex**</span></span>  | <span data-ttu-id="246f8-134">0</span><span class="sxs-lookup"><span data-stu-id="246f8-134">0</span></span>                          |

    

     

    <span data-ttu-id="246f8-135">Поместите точку с запятой в конце строки, которая настраивает эту политику безопасности.</span><span class="sxs-lookup"><span data-stu-id="246f8-135">Place a semicolon at the end of the line configuring this security policy.</span></span> <span data-ttu-id="246f8-136">Записи политики должны быть помещены по убыванию числового порядка.</span><span class="sxs-lookup"><span data-stu-id="246f8-136">The policy entries must be placed in decreasing numerical order.</span></span>

3.  <span data-ttu-id="246f8-137">На узле 1 измените файл SAD, добавив записи SA, чтобы защитить весь трафик между узлом 1 и узлом 2.</span><span class="sxs-lookup"><span data-stu-id="246f8-137">On Host 1, edit the SAD file, adding SA entries to secure all traffic between Host 1 and Host 2.</span></span> <span data-ttu-id="246f8-138">Необходимо создать два сопоставления безопасности: один для трафика на узел 2 и один для трафика с узла 2.</span><span class="sxs-lookup"><span data-stu-id="246f8-138">Two security associations must be created, one for traffic to Host 2 and one for traffic from Host 2.</span></span>

    <span data-ttu-id="246f8-139">В следующей таблице показана первая запись SA, добавленная в файл Test. sad для этого примера (для трафика на узел 2).</span><span class="sxs-lookup"><span data-stu-id="246f8-139">The following table shows the first SA entry added to the Test.sad file for this example (for traffic to Host 2).</span></span>

    | <span data-ttu-id="246f8-140">Имя поля SAD в файле</span><span class="sxs-lookup"><span data-stu-id="246f8-140">SAD file field name</span></span> | <span data-ttu-id="246f8-141">Пример значения</span><span class="sxs-lookup"><span data-stu-id="246f8-141">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="246f8-142">**саентри**</span><span class="sxs-lookup"><span data-stu-id="246f8-142">**SAEntry**</span></span>         | <span data-ttu-id="246f8-143">2</span><span class="sxs-lookup"><span data-stu-id="246f8-143">2</span></span>                          |
    | <span data-ttu-id="246f8-144">**SPI**</span><span class="sxs-lookup"><span data-stu-id="246f8-144">**SPI**</span></span>             | <span data-ttu-id="246f8-145">3001</span><span class="sxs-lookup"><span data-stu-id="246f8-145">3001</span></span>                       |
    | <span data-ttu-id="246f8-146">**садестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-146">**SADestIPAddr**</span></span>    | <span data-ttu-id="246f8-147">**FE80:: 2AA: FF: FE92: D0F1**</span><span class="sxs-lookup"><span data-stu-id="246f8-147">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="246f8-148">**дестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-148">**DestIPAddr**</span></span>      | <span data-ttu-id="246f8-149">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-149">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-150">**срЦипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-150">**SrcIPAddr**</span></span>       | <span data-ttu-id="246f8-151">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-151">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-152">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-152">**Protocol**</span></span>        | <span data-ttu-id="246f8-153">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-153">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-154">**дестпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-154">**DestPort**</span></span>        | <span data-ttu-id="246f8-155">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-155">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-156">**сркпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-156">**SrcPort**</span></span>         | <span data-ttu-id="246f8-157">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-157">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-158">**аусалг**</span><span class="sxs-lookup"><span data-stu-id="246f8-158">**AuthAlg**</span></span>         | <span data-ttu-id="246f8-159">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="246f8-159">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="246f8-160">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="246f8-160">**KeyFile**</span></span>         | <span data-ttu-id="246f8-161">**Тест. ключ**</span><span class="sxs-lookup"><span data-stu-id="246f8-161">**Test.key**</span></span>               |
    | <span data-ttu-id="246f8-162">**Направление**</span><span class="sxs-lookup"><span data-stu-id="246f8-162">**Direction**</span></span>       | <span data-ttu-id="246f8-163">**ХОДЯЩУЮ**</span><span class="sxs-lookup"><span data-stu-id="246f8-163">**OUTBOUND**</span></span>               |
    | <span data-ttu-id="246f8-164">**секполицииндекс**</span><span class="sxs-lookup"><span data-stu-id="246f8-164">**SecPolicyIndex**</span></span>  | <span data-ttu-id="246f8-165">2</span><span class="sxs-lookup"><span data-stu-id="246f8-165">2</span></span>                          |

    

     

    <span data-ttu-id="246f8-166">Поместите точку с запятой в конце строки, которая настраивает это сопоставление безопасности.</span><span class="sxs-lookup"><span data-stu-id="246f8-166">Place a semicolon at the end of the line configuring this SA.</span></span>

    <span data-ttu-id="246f8-167">В следующей таблице показана вторая запись SA, добавленная в файл Test. sad для этого примера (для трафика с узла 2).</span><span class="sxs-lookup"><span data-stu-id="246f8-167">The following table shows the second SA entry added to the Test.sad file for this example (for traffic from Host 2).</span></span>

    | <span data-ttu-id="246f8-168">Имя поля SAD в файле</span><span class="sxs-lookup"><span data-stu-id="246f8-168">SAD file field name</span></span> | <span data-ttu-id="246f8-169">Пример значения</span><span class="sxs-lookup"><span data-stu-id="246f8-169">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="246f8-170">**саентри**</span><span class="sxs-lookup"><span data-stu-id="246f8-170">**SAEntry**</span></span>         | <span data-ttu-id="246f8-171">1</span><span class="sxs-lookup"><span data-stu-id="246f8-171">1</span></span>                          |
    | <span data-ttu-id="246f8-172">**SPI**</span><span class="sxs-lookup"><span data-stu-id="246f8-172">**SPI**</span></span>             | <span data-ttu-id="246f8-173">3000</span><span class="sxs-lookup"><span data-stu-id="246f8-173">3000</span></span>                       |
    | <span data-ttu-id="246f8-174">**садестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-174">**SADestIPAddr**</span></span>    | <span data-ttu-id="246f8-175">**FE80:: 2AA: FF: FE53: A92C**</span><span class="sxs-lookup"><span data-stu-id="246f8-175">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="246f8-176">**дестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-176">**DestIPAddr**</span></span>      | <span data-ttu-id="246f8-177">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-177">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-178">**срЦипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-178">**SrcIPAddr**</span></span>       | <span data-ttu-id="246f8-179">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-179">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-180">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-180">**Protocol**</span></span>        | <span data-ttu-id="246f8-181">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-181">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-182">**дестпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-182">**DestPort**</span></span>        | <span data-ttu-id="246f8-183">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-183">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-184">**сркпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-184">**SrcPort**</span></span>         | <span data-ttu-id="246f8-185">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-185">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-186">**аусалг**</span><span class="sxs-lookup"><span data-stu-id="246f8-186">**AuthAlg**</span></span>         | <span data-ttu-id="246f8-187">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="246f8-187">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="246f8-188">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="246f8-188">**KeyFile**</span></span>         | <span data-ttu-id="246f8-189">**Тест. ключ**</span><span class="sxs-lookup"><span data-stu-id="246f8-189">**Test.key**</span></span>               |
    | <span data-ttu-id="246f8-190">**Направление**</span><span class="sxs-lookup"><span data-stu-id="246f8-190">**Direction**</span></span>       | <span data-ttu-id="246f8-191">**ТРАФИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-191">**INBOUND**</span></span>                |
    | <span data-ttu-id="246f8-192">**секполицииндекс**</span><span class="sxs-lookup"><span data-stu-id="246f8-192">**SecPolicyIndex**</span></span>  | <span data-ttu-id="246f8-193">2</span><span class="sxs-lookup"><span data-stu-id="246f8-193">2</span></span>                          |

    

     

    <span data-ttu-id="246f8-194">Поместите точку с запятой в конце строки, которая настраивает это сопоставление безопасности.</span><span class="sxs-lookup"><span data-stu-id="246f8-194">Place a semicolon at the end of the line configuring this SA.</span></span> <span data-ttu-id="246f8-195">Записи SA должны быть помещены в порядке убывания числовых значений.</span><span class="sxs-lookup"><span data-stu-id="246f8-195">The SA entries must be placed in decreasing numerical order.</span></span>

4.  <span data-ttu-id="246f8-196">На узле 1 Создайте текстовый файл, содержащий текстовую строку, используемую для проверки подлинности SAs, созданной с помощью узла 2.</span><span class="sxs-lookup"><span data-stu-id="246f8-196">On Host 1, create a text file that contains a text string used to authenticate the SAs created with Host 2.</span></span> <span data-ttu-id="246f8-197">В этом примере создается файл Test. Key с содержимым «это тест».</span><span class="sxs-lookup"><span data-stu-id="246f8-197">In this example, the file Test.key is created with the contents "This is a test".</span></span> <span data-ttu-id="246f8-198">Чтобы ключ можно было прочитать с помощью средства Ipsec6, необходимо добавить ключ в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="246f8-198">You must include double quotes around the key string in order for the key to be read by the ipsec6 tool.</span></span>

    <span data-ttu-id="246f8-199">Предварительная версия Microsoft IPv6 Technology Preview поддерживает только вручную настроенные ключи для проверки подлинности SAs IPsec.</span><span class="sxs-lookup"><span data-stu-id="246f8-199">The Microsoft IPv6 Technology Preview only supports manually configured keys for the authentication of IPsec SAs.</span></span> <span data-ttu-id="246f8-200">Ключи вручную настраиваются путем создания текстовых файлов, содержащих текстовую строку ключа вручную.</span><span class="sxs-lookup"><span data-stu-id="246f8-200">The manual keys are configured by creating text files that contain the text string of the manual key.</span></span> <span data-ttu-id="246f8-201">В этом примере один и тот же ключ для SAs используется в обоих направлениях.</span><span class="sxs-lookup"><span data-stu-id="246f8-201">In this example, the same key for the SAs is used in both directions.</span></span> <span data-ttu-id="246f8-202">Вы можете использовать разные ключи для входящей и исходящей SAs, создав разные файлы ключей и ссылаясь на них с помощью поля KeyFile в файле SAD.</span><span class="sxs-lookup"><span data-stu-id="246f8-202">You can use different keys for inbound and outbound SAs by creating different key files and referencing them with the KeyFile field in the SAD file.</span></span>

5.  <span data-ttu-id="246f8-203">На узле 2 создайте пустые файлы сопоставления безопасности (SAD) и политики безопасности (SPD) с помощью команды ipsec6 c.</span><span class="sxs-lookup"><span data-stu-id="246f8-203">On Host 2, create blank security association (SAD) and security policy (SPD) files by using the ipsec6 c command.</span></span> <span data-ttu-id="246f8-204">В этом примере команда Ipsec6.exe ipsec6 Test c.</span><span class="sxs-lookup"><span data-stu-id="246f8-204">In this example, the Ipsec6.exe command is ipsec6 c test.</span></span> <span data-ttu-id="246f8-205">При этом создаются два файла с пустыми записями для ручной настройки сопоставлений безопасности (Test. sad) и политик безопасности (Test. SPD).</span><span class="sxs-lookup"><span data-stu-id="246f8-205">This creates two files with blank entries for manually configuring security associations (Test.sad) and security policies (Test.spd).</span></span>

    <span data-ttu-id="246f8-206">Для упрощения примера на узле 2 используются те же имена файлов для файлов SAD и SPD.</span><span class="sxs-lookup"><span data-stu-id="246f8-206">To simplify the example, the same file names for the SAD and SPD files are used on Host 2.</span></span> <span data-ttu-id="246f8-207">На каждом узле можно использовать разные имена файлов.</span><span class="sxs-lookup"><span data-stu-id="246f8-207">You can choose to use different file names on each host.</span></span>

6.  <span data-ttu-id="246f8-208">На узле 2 Измените файл SPD, добавив политику безопасности, которая защищает весь трафик между узлом 2 и узлом 1.</span><span class="sxs-lookup"><span data-stu-id="246f8-208">On Host 2, edit the SPD file to add a security policy that secures all traffic between Host 2 and Host 1.</span></span>

    <span data-ttu-id="246f8-209">В следующей таблице показана запись политики безопасности, добавленная перед первой записью в файл Test. SPD для этого примера (первая запись в файле Test. SPD не была изменена).</span><span class="sxs-lookup"><span data-stu-id="246f8-209">The following table shows the security policy entry added before the first entry to the Test.spd file for this example (the first entry in the Test.spd file was not modified).</span></span>

    | <span data-ttu-id="246f8-210">Имя поля в файле SPD</span><span class="sxs-lookup"><span data-stu-id="246f8-210">SPD file field name</span></span> | <span data-ttu-id="246f8-211">Пример значения</span><span class="sxs-lookup"><span data-stu-id="246f8-211">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="246f8-212">**Политика**</span><span class="sxs-lookup"><span data-stu-id="246f8-212">**Policy**</span></span>          | <span data-ttu-id="246f8-213">2</span><span class="sxs-lookup"><span data-stu-id="246f8-213">2</span></span>                          |
    | <span data-ttu-id="246f8-214">**ремотеипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-214">**RemoteIPAddr**</span></span>    | <span data-ttu-id="246f8-215">**FE80:: 2AA: FF: FE53: A92C**</span><span class="sxs-lookup"><span data-stu-id="246f8-215">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="246f8-216">**локалипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-216">**LocalIPAddr**</span></span>     | \*                         |
    | <span data-ttu-id="246f8-217">**ремотепорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-217">**RemotePort**</span></span>      | \*                         |
    | <span data-ttu-id="246f8-218">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-218">**Protocol**</span></span>        | \*                         |
    | <span data-ttu-id="246f8-219">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="246f8-219">**LocalPort**</span></span>       | \*                         |
    | <span data-ttu-id="246f8-220">**ипсекпротокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-220">**IPSecProtocol**</span></span>   | <span data-ttu-id="246f8-221">**ЗАГОЛОВКИ**</span><span class="sxs-lookup"><span data-stu-id="246f8-221">**AH**</span></span>                     |
    | <span data-ttu-id="246f8-222">**ипсекмоде**</span><span class="sxs-lookup"><span data-stu-id="246f8-222">**IPSecMode**</span></span>       | <span data-ttu-id="246f8-223">**ПЕРЕМЕЩЕНИЯ**</span><span class="sxs-lookup"><span data-stu-id="246f8-223">**TRANSPORT**</span></span>              |
    | <span data-ttu-id="246f8-224">**ремотегвипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-224">**RemoteGWIPAddr**</span></span>  | \*                         |
    | <span data-ttu-id="246f8-225">**сабундлеиндекс**</span><span class="sxs-lookup"><span data-stu-id="246f8-225">**SABundleIndex**</span></span>   | <span data-ttu-id="246f8-226">**NONE**</span><span class="sxs-lookup"><span data-stu-id="246f8-226">**NONE**</span></span>                   |
    | <span data-ttu-id="246f8-227">**Направление**</span><span class="sxs-lookup"><span data-stu-id="246f8-227">**Direction**</span></span>       | <span data-ttu-id="246f8-228">**бидирект**</span><span class="sxs-lookup"><span data-stu-id="246f8-228">**BIDIRECT**</span></span>               |
    | <span data-ttu-id="246f8-229">**Действие**</span><span class="sxs-lookup"><span data-stu-id="246f8-229">**Action**</span></span>          | <span data-ttu-id="246f8-230">**КАСАТЬСЯ**</span><span class="sxs-lookup"><span data-stu-id="246f8-230">**APPLY**</span></span>                  |
    | <span data-ttu-id="246f8-231">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="246f8-231">**InterfaceIndex**</span></span>  | <span data-ttu-id="246f8-232">0</span><span class="sxs-lookup"><span data-stu-id="246f8-232">0</span></span>                          |

    

     

    <span data-ttu-id="246f8-233">Поместите точку с запятой в конце строки, которая настраивает эту политику безопасности.</span><span class="sxs-lookup"><span data-stu-id="246f8-233">Place a semicolon at the end of the line configuring this security policy.</span></span> <span data-ttu-id="246f8-234">Записи политики должны быть помещены по убыванию числового порядка.</span><span class="sxs-lookup"><span data-stu-id="246f8-234">The policy entries must be placed in decreasing numerical order.</span></span>

7.  <span data-ttu-id="246f8-235">На узле 2 Измените файл SAD, добавив записи SA, чтобы защитить весь трафик между узлом 2 и узлом 1.</span><span class="sxs-lookup"><span data-stu-id="246f8-235">On Host 2, edit the SAD file, adding SA entries to secure all traffic between Host 2 and Host 1.</span></span> <span data-ttu-id="246f8-236">Необходимо создать два сопоставления безопасности — один для трафика на узел 1 и один для трафика от узла 1.</span><span class="sxs-lookup"><span data-stu-id="246f8-236">Two security associations must be created-one for traffic to Host 1 and one for traffic from Host 1.</span></span>

    <span data-ttu-id="246f8-237">В следующей таблице показано первое сопоставление SA, добавленное в файл Test. SAD, для этого примера (для трафика с узла 1).</span><span class="sxs-lookup"><span data-stu-id="246f8-237">The following table shows the first SA added to the Test.sad file for this example (for traffic from Host 1).</span></span>

    | <span data-ttu-id="246f8-238">Имя поля SAD в файле</span><span class="sxs-lookup"><span data-stu-id="246f8-238">SAD file field name</span></span> | <span data-ttu-id="246f8-239">Пример значения</span><span class="sxs-lookup"><span data-stu-id="246f8-239">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="246f8-240">**саентри**</span><span class="sxs-lookup"><span data-stu-id="246f8-240">**SAEntry**</span></span>         | <span data-ttu-id="246f8-241">2</span><span class="sxs-lookup"><span data-stu-id="246f8-241">2</span></span>                          |
    | <span data-ttu-id="246f8-242">**SPI**</span><span class="sxs-lookup"><span data-stu-id="246f8-242">**SPI**</span></span>             | <span data-ttu-id="246f8-243">3001</span><span class="sxs-lookup"><span data-stu-id="246f8-243">3001</span></span>                       |
    | <span data-ttu-id="246f8-244">**садестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-244">**SADestIPAddr**</span></span>    | <span data-ttu-id="246f8-245">**FE80:: 2AA: FF: FE92: D0F1**</span><span class="sxs-lookup"><span data-stu-id="246f8-245">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="246f8-246">**дестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-246">**DestIPAddr**</span></span>      | <span data-ttu-id="246f8-247">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-247">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-248">**срЦипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-248">**SrcIPAddr**</span></span>       | <span data-ttu-id="246f8-249">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-249">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-250">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-250">**Protocol**</span></span>        | <span data-ttu-id="246f8-251">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-251">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-252">**дестпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-252">**DestPort**</span></span>        | <span data-ttu-id="246f8-253">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-253">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-254">**сркпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-254">**SrcPort**</span></span>         | <span data-ttu-id="246f8-255">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-255">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-256">**аусалг**</span><span class="sxs-lookup"><span data-stu-id="246f8-256">**AuthAlg**</span></span>         | <span data-ttu-id="246f8-257">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="246f8-257">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="246f8-258">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="246f8-258">**KeyFile**</span></span>         | <span data-ttu-id="246f8-259">**Тест. ключ**</span><span class="sxs-lookup"><span data-stu-id="246f8-259">**Test.key**</span></span>               |
    | <span data-ttu-id="246f8-260">**Направление**</span><span class="sxs-lookup"><span data-stu-id="246f8-260">**Direction**</span></span>       | <span data-ttu-id="246f8-261">**ТРАФИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-261">**INBOUND**</span></span>                |
    | <span data-ttu-id="246f8-262">**секполицииндекс**</span><span class="sxs-lookup"><span data-stu-id="246f8-262">**SecPolicyIndex**</span></span>  | <span data-ttu-id="246f8-263">2</span><span class="sxs-lookup"><span data-stu-id="246f8-263">2</span></span>                          |

    

     

    <span data-ttu-id="246f8-264">Поместите точку с запятой в конце строки, которая настраивает это сопоставление безопасности.</span><span class="sxs-lookup"><span data-stu-id="246f8-264">Place a semicolon at the end of the line configuring this SA.</span></span>

    <span data-ttu-id="246f8-265">В следующей таблице показана вторая запись SA, добавленная в файл Test. sad для этого примера (для трафика на узел 1).</span><span class="sxs-lookup"><span data-stu-id="246f8-265">The following table shows the second SA entry added to the Test.sad file for this example (for traffic to Host 1).</span></span>

    | <span data-ttu-id="246f8-266">Имя поля SAD в файле</span><span class="sxs-lookup"><span data-stu-id="246f8-266">SAD file field name</span></span> | <span data-ttu-id="246f8-267">Пример значения</span><span class="sxs-lookup"><span data-stu-id="246f8-267">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="246f8-268">**саентри**</span><span class="sxs-lookup"><span data-stu-id="246f8-268">**SAEntry**</span></span>         | <span data-ttu-id="246f8-269">1</span><span class="sxs-lookup"><span data-stu-id="246f8-269">1</span></span>                          |
    | <span data-ttu-id="246f8-270">**SPI**</span><span class="sxs-lookup"><span data-stu-id="246f8-270">**SPI**</span></span>             | <span data-ttu-id="246f8-271">3000</span><span class="sxs-lookup"><span data-stu-id="246f8-271">3000</span></span>                       |
    | <span data-ttu-id="246f8-272">**садестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-272">**SADestIPAddr**</span></span>    | <span data-ttu-id="246f8-273">**FE80:: 2AA: FF: FE53: A92C**</span><span class="sxs-lookup"><span data-stu-id="246f8-273">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="246f8-274">**дестипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-274">**DestIPAddr**</span></span>      | <span data-ttu-id="246f8-275">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-275">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-276">**срЦипаддр**</span><span class="sxs-lookup"><span data-stu-id="246f8-276">**SrcIPAddr**</span></span>       | <span data-ttu-id="246f8-277">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-277">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-278">**Протокол**</span><span class="sxs-lookup"><span data-stu-id="246f8-278">**Protocol**</span></span>        | <span data-ttu-id="246f8-279">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-279">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-280">**дестпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-280">**DestPort**</span></span>        | <span data-ttu-id="246f8-281">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-281">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-282">**сркпорт**</span><span class="sxs-lookup"><span data-stu-id="246f8-282">**SrcPort**</span></span>         | <span data-ttu-id="246f8-283">**ПОЛИТИКА**</span><span class="sxs-lookup"><span data-stu-id="246f8-283">**POLICY**</span></span>                 |
    | <span data-ttu-id="246f8-284">**аусалг**</span><span class="sxs-lookup"><span data-stu-id="246f8-284">**AuthAlg**</span></span>         | <span data-ttu-id="246f8-285">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="246f8-285">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="246f8-286">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="246f8-286">**KeyFile**</span></span>         | <span data-ttu-id="246f8-287">**Тест. ключ**</span><span class="sxs-lookup"><span data-stu-id="246f8-287">**Test.key**</span></span>               |
    | <span data-ttu-id="246f8-288">**Направление**</span><span class="sxs-lookup"><span data-stu-id="246f8-288">**Direction**</span></span>       | <span data-ttu-id="246f8-289">**ХОДЯЩУЮ**</span><span class="sxs-lookup"><span data-stu-id="246f8-289">**OUTBOUND**</span></span>               |
    | <span data-ttu-id="246f8-290">**секполицииндекс**</span><span class="sxs-lookup"><span data-stu-id="246f8-290">**SecPolicyIndex**</span></span>  | <span data-ttu-id="246f8-291">2</span><span class="sxs-lookup"><span data-stu-id="246f8-291">2</span></span>                          |

    

     

    <span data-ttu-id="246f8-292">Поместите точку с запятой в конце строки, которая настраивает это сопоставление безопасности.</span><span class="sxs-lookup"><span data-stu-id="246f8-292">Place a semicolon at the end of the line configuring this SA.</span></span> <span data-ttu-id="246f8-293">Записи SA должны быть помещены в порядке убывания числовых значений.</span><span class="sxs-lookup"><span data-stu-id="246f8-293">The SA entries must be placed in decreasing numerical order.</span></span>

8.  <span data-ttu-id="246f8-294">На узле 2 Создайте текстовый файл, содержащий текстовую строку, используемую для проверки подлинности SAs, созданной с помощью узла 1.</span><span class="sxs-lookup"><span data-stu-id="246f8-294">On Host 2, create a text file that contains a text string used to authenticate the SAs created with Host 1.</span></span> <span data-ttu-id="246f8-295">В этом примере создается файл Test. Key с содержимым «это тест».</span><span class="sxs-lookup"><span data-stu-id="246f8-295">In this example, the file Test.key is created with the contents "This is a test".</span></span> <span data-ttu-id="246f8-296">Чтобы ключ можно было прочитать с помощью средства Ipsec6, необходимо добавить ключ в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="246f8-296">You must include double quotes around the key string in order for the key to be read by the ipsec6 tool.</span></span>
9.  <span data-ttu-id="246f8-297">На узле 1 Добавьте настроенные политики безопасности и SAs из файлов SPD и SAD с помощью команды ipsec6.</span><span class="sxs-lookup"><span data-stu-id="246f8-297">On Host 1, add the configured security policies and SAs from the SPD and SAD files using the ipsec6 a command.</span></span> <span data-ttu-id="246f8-298">В этом примере на узле 1 выполняется команда TEST ipsec6.</span><span class="sxs-lookup"><span data-stu-id="246f8-298">In this example, the ipsec6 a test command is run on Host 1.</span></span>
10. <span data-ttu-id="246f8-299">На узле 2 Добавьте настроенные политики безопасности и SAs из файлов SPD и SAD с помощью команды ipsec6.</span><span class="sxs-lookup"><span data-stu-id="246f8-299">On Host 2, add the configured security policies and SAs from the SPD and SAD files by using the ipsec6 a command.</span></span> <span data-ttu-id="246f8-300">В этом примере на узле 2 выполняется команда ipsec6.</span><span class="sxs-lookup"><span data-stu-id="246f8-300">In this example, the ipsec6 a test command is run on Host 2.</span></span>
11. <span data-ttu-id="246f8-301">Проверка связи с узлом 1 с узла 2 с помощью команды ping6.</span><span class="sxs-lookup"><span data-stu-id="246f8-301">Ping Host 1 from Host 2 with the ping6 command.</span></span>

    <span data-ttu-id="246f8-302">Если вы захватываете трафик с помощью Microsoft Network Monitor или другого средства прослушивания пакетов, вы должны увидеть обмен сообщениями эхо-запроса ICMPv6 и эхо-ответа с заголовком проверки подлинности между заголовком IPv6 и заголовком ICMPv6.</span><span class="sxs-lookup"><span data-stu-id="246f8-302">If you capture the traffic using Microsoft Network Monitor or another packet sniffer, you should see the exchange of ICMPv6 Echo Request and Echo Reply messages with an Authentication Header between the IPv6 header and the ICMPv6 header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="246f8-303">См. также</span><span class="sxs-lookup"><span data-stu-id="246f8-303">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="246f8-304">Рекомендуемые конфигурации для IPv6</span><span class="sxs-lookup"><span data-stu-id="246f8-304">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="246f8-305">Одна подсеть с адресами локальной связи</span><span class="sxs-lookup"><span data-stu-id="246f8-305">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="246f8-306">Трафик IPv6 между узлами в разных подсетях объединенной сети IPv4 (6to4)</span><span class="sxs-lookup"><span data-stu-id="246f8-306">IPv6 traffic between nodes on different subnets of an IPv4 internetwork (6to4)</span></span>](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



