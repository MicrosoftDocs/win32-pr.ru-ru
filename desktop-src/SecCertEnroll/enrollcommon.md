---
description: Папка Енроллкоммон содержит следующие вспомогательные функции и макросы, используемые в примерах, предоставляемых с помощью пакета SDK для регистрации сертификатов.
ms.assetid: a9b3532d-9640-4373-a6c6-7828cb6f55c7
title: енроллкоммон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384a1f3741fd8bd7762c60da524e2e639c442e41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542690"
---
# <a name="enrollcommon"></a>енроллкоммон

Папка Енроллкоммон содержит следующие вспомогательные функции и макросы, используемые в примерах, предоставляемых с помощью пакета SDK для регистрации сертификатов. Он устанавливается по умолчанию в папке *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ Certificate енроллкоммон сертификата \\ X509 \\ .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Функция</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>_JumpIfError</td>
<td>Макрос, принимающий значение <strong>HRESULT</strong> , метку и строку ошибки, выводит строку и передает управление программой первому оператору, следующему за меткой.</td>
</tr>
<tr class="even">
<td>_JumpError</td>
<td>То же, что и макрос _JumpIfError.</td>
</tr>
<tr class="odd">
<td>_PrintIfError</td>
<td>В настоящий момент не используется.</td>
</tr>
<tr class="even">
<td>_PrintError</td>
<td>Макрос, который выводит сообщение об ошибке и значение <strong>HRESULT</strong> .</td>
</tr>
<tr class="odd">
<td>конвертвсзтосз</td>
<td>Преобразует строку расширенных символов в строку символов ASCII с помощью функции <strong>WideCharToMultiByte</strong> и текущего идентификатора кодовой страницы ANSI для системы. Эта функция используется функциями Декконвертфромуникоде и Финдоидфромтемплатенаме, определенными в Енроллкоммон. cpp.</td>
</tr>
<tr class="even">
<td>конвертсзтовсз</td>
<td>Преобразует строку ASCII в строку расширенных символов с помощью функции <strong>MultiByteToWideChar</strong> и идентификатора текущей кодовой страницы ANSI для системы. Эта функция используется функцией Финдцертбитемплате, определенной в Енроллкоммон. cpp.</td>
</tr>
<tr class="odd">
<td>конвертсзтобстр</td>
<td>Преобразует строку ASCII в <strong>BSTR</strong> с помощью функции <strong>MultiByteToWideChar</strong> . Эта функция в настоящее время не используется.</td>
</tr>
<tr class="even">
<td>конвертвсзтобстр</td>
<td>Преобразует строку расширенных символов в <strong>BSTR</strong>. Эта функция используется примером Инсталлреспонсефромпфкс.</td>
</tr>
<tr class="odd">
<td>чеккенроллстатус</td>
<td>Проверяет состояние процесса регистрации сертификата с помощью интерфейсов <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> и <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus"><strong>IX509EnrollmentStatus</strong></a> . Эта функция используется в примерах Енроллеобокмк, enrollPKCS7, enrollRenewalPKCS7, Енроллсимплемачинецерт и Енроллсимплеусерцерт.</td>
</tr>
<tr class="even">
<td>финдцертбикэйусаже</td>
<td>Перечисляет личное хранилище сертификатов текущего пользователя, чтобы найти первый сертификат, для которого предполагаемое использование открытого ключа соответствует указанному значению. Указанное значение может быть побитовым сочетанием следующих флагов:
<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>
Эта функция используется примером Енроллфромпубликкэй.<br/></td>
</tr>
<tr class="odd">
<td>финдцертбеку</td>
<td>Перечисляет личное хранилище сертификатов текущего пользователя, чтобы найти первый сертификат, для которого расширение расширенного использования ключа (EKU) соответствует указанному во входных данных. Дополнительные сведения о расширении EKU см. в разделе интерфейс <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage"><strong>IX509ExtensionEnhancedKeyUsage</strong></a> . Эта функция используется примером Енроллеобокмк.</td>
</tr>
<tr class="even">
<td>финдцертбитемплате</td>
<td>Перечисляет личное хранилище сертификатов текущего пользователя, чтобы найти первый сертификат, для которого шаблон соответствует указанному по имени, на входе. Эта функция используется в примерах enrollPKCS7 и enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>енроллцертбитемплате</td>
<td>Инициализирует объект <a href="/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment"><strong>IX509Enrollment</strong></a> с помощью шаблона, пытается зарегистрировать неявно созданный запрос на сертификат и отслеживает состояние процесса регистрации. Эта функция используется в примерах Енроллеобокмк, Енроллфромпубликкэй, enrollPKCS7 и enrollRenewalPKCS7.</td>
</tr>
<tr class="even">
<td>верифицертконтекст</td>
<td>Проверяет соответствие цепочки сертификатов указанной (базовой) политике и (необязательно) для указанного расширения расширенного использования ключа (EKU). Дополнительные сведения см. в разделе Функция <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy"><strong>цертверифицертификатечаинполици</strong></a> и структуры <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_policy_para"><strong>CERT_CHAIN_POLICY_PARA</strong></a> и <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_para"><strong>CERT_CHAIN_PARA</strong></a> . Эта функция используется в примерах Енроллеобокмк, Енроллфромпубликкэй, enrollPKCS7 и enrollRenewalPKCS7.</td>
</tr>
<tr class="odd">
<td>декконвертфромуникоде</td>
<td>Преобразует строку двухбайтовых символов Юникода в строку однобайтовых символов ANSI. Эта функция используется функцией Декодефилев, определенной в Енроллкоммон. cpp.</td>
</tr>
<tr class="even">
<td>декодефилев</td>
<td>Декодирует закодированный сертификат или файл запроса на сертификат в массив байтов. Эта функция используется примером Инсталлреспонсефромпфкс.</td>
</tr>
<tr class="odd">
<td>енкодетофилев</td>
<td>Кодирует сертификат или запрос на сертификат и сохраняет его в файл. Эта функция используется в примерах Креатекнгкустомкмк, Енроллеобокмк и Енроллфромпубликкэй.</td>
</tr>
<tr class="even">
<td>финдоидфромтемплатенаме</td>
<td>Возвращает идентификатор объекта для шаблона, указанного по имени. Эта функция используется функцией Финдцертбитемплате, определенной в Енроллкоммон. cpp.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование прилагаемых примеров](using-the-included-samples.md)
</dt> </dl>

 

