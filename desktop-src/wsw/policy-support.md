---
title: Поддержка политик
description: Всутил обрабатывает политику, указанную во входных метаданных, и создает вспомогательные подпрограммы для поддержки модели службы.
ms.assetid: 9c4fb485-2392-4117-b4a7-7a51786d60b9
keywords:
- Веб-службы поддержки политик для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 347265d4081216a227b5040fc73f272181bdccfe09ca7500b81078a6a57ed7bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838644"
---
# <a name="policy-support"></a>Поддержка политик

Всутил обрабатывает политику, указанную во входных метаданных, и создает вспомогательные подпрограммы для поддержки модели службы.

## <a name="how-to-use-policy-support-in-wsutil"></a>Использование поддержки политик в всутил

Чтобы использовать поддержку политики в компиляторе всутил, разработчикам необходимо выполнить следующие действия.

-   Собирайте все файлы входных метаданных, необходимые для целевой веб-службы.
-   Скомпилируйте все собранные файлы WSDL/XSD/Policy с помощью wsutil.exe. Всутил создает один набор файлов-заглушек и файл заголовка для всех входных файлов WSDL и XSD.
-   Проверьте созданный файл заголовка. все имена вспомогательных подпрограмм политики перечислены в разделе комментариев в начале файла заголовка.
-   Используйте \_ вспомогательную подпрограммы биндингнаме креатесервицепрокси для создания прокси-сервера службы.
-   \_Для создания конечной точки службы используйте вспомогательную подпрограммы биндингнаме креатесервицеендпоинт.
-   Заполните \_ \_ структуру шаблона привязки WS биндингтемплатетипе \_ , указанную в сигнатуре метода. При необходимости разработчики могут предоставлять дополнительные свойства канала и (или) свойства безопасности.
-   Вызов вспомогательных подпрограмм, при успешном возвращении прокси-сервера службы возврата или конечной точки службы.

В следующих разделах подробно описаны связанные разделы.

## <a name="handle-policy-input"></a>Работа с входными данными политики

Ниже приведены [параметры компилятора](web-service-compiler-tool.md) , связанные с обработкой политики.

По умолчанию всутил всегда создает шаблоны политик, если не вызывается с параметром "/нополици". Политику можно внедрить как часть WSDL-файла или создать отдельно в качестве файла метаданных политики, который всутил принимает в качестве входных данных. Параметр компилятора "/ВСП:" используется для указания того, что указанные входные метаданные являются файлом политики. Всутил создает потенциальные вспомогательные методы, связанные с политикой, со следующей компиляцией:

**всутил/всдл: Trusted. WSDL/всдл: TRUSTED1. WSDL**

**встуил/всдл: input. WSDL/ВСП: Policy. wsp**

При использовании параметра "/нополици" вспомогательные методы политики не создаются, как показано в следующем примере.

**всутил/нополици/всдл: Trusted. WSDL/всдл: TRUSTED1. WSDL**

## <a name="policy-related-code-generated-by-the-wsutil-compiler"></a>Код, связанный с политикой, созданный компилятором всутил

Страница [сопоставления метаданных](metadata-mapping.md) содержит сведения о сопоставлении между конструкциями метаданных и различными типами привязок.

В параметрах политики можно указать три категории параметров политики:

-   Свойства канала. В настоящее время поддерживаются только следующие свойства канала [**: \_ \_ \_ Кодировка свойства канала WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id), **\_ \_ \_ \_ Версия адресации свойства канала WS** и **\_ \_ \_ \_ Версия конверта свойства WS Channel**.
-   Свойства безопасности. В настоящее время поддерживаются только следующие свойства безопасности: [**Служба WS \_ Security \_ свойство \_ timestamp \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id), **\_ \_ \_ \_ \_ макет заголовка безопасности свойства** WS Security **, \_ \_ \_ \_ \_ уровень защиты транспорта** и **\_ \_ \_ \_ \_ версия заголовка безопасности свойства WS Security**.
-   Привязка безопасности. В настоящее время поддерживаются только следующие привязки безопасности: [**\_ \_ \_ \_ \_ Привязка безопасности HTTP-заголовка**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)Authentication, привязка безопасности [**\_ \_ транспорта \_ WS \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding), привязка безопасности WS [**\_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding), привязка [**безопасности \_ \_ сообщений имени \_ пользователя \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding), привязка [**безопасности \_ сообщений WS Kerberos \_ апрек \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)и [**\_ \_ \_ \_ \_ Привязка безопасности сообщений контекста безопасности**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)сообщения.

Тип шаблона привязки

Существует ограниченное количество привязок, поддерживаемых в всутил. Все поддерживаемые сочетания этих привязок перечислены в определении [**\_ \_ \_ типа шаблона привязки WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) . Например, для следующей привязки в WSDL

``` syntax
<soap:binding style="document" transport="http://schemas.xmlsoap.org/soap/http" />
```

Всутил создает тип шаблона привязки [**WS \_ http Binding \_ \_ \_ Type**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) для этой привязки.

Описания политик

С параметром входной политики всутил формирует набор описаний политик, описывающих входную политику, включая тип шаблона, а также значения, указанные в политике. Например, для входных данных

``` syntax
<wsdl:binding...>
  <soap11:binding.../> =< WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

всутил создает описание свойства канала, например:

``` syntax
WS_ENVELOPE_VERSION_SOAP_1_1,
{
  WS_CHANNEL_PROPERTY_ENVELOPE_VERSION,
  (void*)&locaDefinitions.policies.bindHostedClientSoap.envelopeVersion, //points to the WS_ENVELOPE_VERSION_SOAP_1_1 value above
  sizeof(&localDefinitions.policies.bindHostedClientSoap.envelopeVersion),
},
```

Все параметры политики (свойства канала, свойства безопасности и свойства привязки безопасности) в одной привязке объединены в одну \_ \_ структуру описания политики WS биндингтемплатетипе \_ . [**Служба WS \_ \_ \_ Тип шаблона привязки**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) указывает различные сочетания политик привязки, поддерживаемые всутил.

Структура шаблона, заполняемая приложением

Описание политики содержит все сведения о политике, указанные во входных метаданных для данной привязки, но сведения, которые не могут быть представлены в политике, требуют ввода данных пользователем при использовании этих параметров политики для создания прокси-сервера службы или конечной точки службы. Например, приложение должно предоставить учетные данные для проверки подлинности заголовка HTTP.

Приложению необходимо заполнить структуру шаблона с именем " \_ \_ шаблон привязки WS биндингтемплатетипе \_ " для каждого типа шаблона привязки, определенного в веб-службах. h:

``` syntax
struct WS_bindingTemplateType_BINDING_TEMPLATE
{
  WS_CHANNEL_PROPERTIES channelProperties;
  WS_SECURITY_PROPERTIES securityProperties;
  possible_list_of_SECURITY_BINDING_TEMPLATEs;
  ...
};
```

Список шаблонов привязки безопасности является необязательным, зависит от соответствующей привязки безопасности. Например, поле [**\_ \_ \_ \_ \_ шаблона привязки безопасности транспорта WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template) представлено в [**\_ \_ \_ \_ шаблоне привязки WS HTTP SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) для приложения, которое предоставляет сведения о привязке безопасности, связанные с SSL, включая учетные данные.

Приложению необходимо заполнить все поля в этой структуре перед вызовом API-интерфейсов шаблонов WebService. Дополнительные свойства безопасности, а также свойства привязки безопасности, которые не могут быть представлены в политике, должны быть заполнены, а API-интерфейсы WebService объединяют два набора свойств во время выполнения. Поля могут быть обнулены, если они не применимы. Например, Секуритипропертиес может быть обнулен, если дополнительные свойства безопасности не требуются.

Вспомогательные подпрограммы и объявление описания политики в файлах заголовков

всутил создает вспомогательную подпрограммы для упрощения поддержки уровня модели служб, что позволяет упростить создание прокси-сервера службы и конечной точки службы. Описание политики также предоставляется для того, чтобы приложение может использовать их напрямую. Процедура справки Креатесеривцепрокси выглядит следующим образом:

``` syntax
HRESULT bindingName_CreateServiceProxy(
  __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
  __in const ULONG propertyCount,
  __in WS_constraintName_BINDING_TEMPLATE* templateValue,
  __deref_out WS_SERVICE_PROXY** serviceProxy,
  __in_opt WS_ERROR* error);
```

Разработчикам рекомендуется использовать эти вспомогательные подпрограммы, хотя они также могут напрямую использовать подпрограмму среды выполнения, предоставляемую webservices.dll. Разработчикам не рекомендуется использовать описания политик непосредственно при программировании с использованием уровня [модели службы](service-model-layer-overview.md) .

В заголовке для опытных пользователей также создаются ссылки на описание политики. Если разработчики не используют функциональные возможности модели служб, они могут использовать описания политик напрямую.

``` syntax
struct {
  ...
  struct {
    ...
    } contracts;
  struct {
    WS_bindingTemplateType_POLICY_DESCRIPTION bindingName;
    ...
    } policies;
  }
```

Прототипы определений в файлах заглушек

Отдельное поле структуры описания политики для каждой привязки и внутренних вспомогательных описаний создается в локальной структуре прототипа. Описания политик создаются в файле, в котором создается [**\_ \_ Описание контракта WS**](/windows/desktop/api/WebServices/ns-webservices-ws_contract_description) . Обычно разработчикам не нужно проверять файл заглушки во время разработки, хотя файл заглушки содержит все сведения о спецификациях политики.

``` syntax
struct {
  ...
  struct {
  ... } contracts;
  ...
 struct {
      struct {
        hierarchy of policy template descriptions;
        } bindingName;
      ...
      list of bindings in the input wsdl file.
  } policies;
} fileNameLocalDefinitions;
```

Реализация вспомогательных подпрограмм в файлах-заглушекх

Всутил создает вспомогательные подпрограммы для упрощения вызовов приложений в [**вскреатесервицепрокси**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) и создания базы [**\_ \_ конечной точки службы WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) на основе сведений, предоставленных в параметрах политики.

Зависит от ограничений привязки, заданных для данного порта, первый аргумент отличается в соответствии со структурой шаблона. В следующем примере предполагается транспорт HTTP, подпись для создания прокси-сервера службы аналогична одному дополнительному параметру типа канала.

``` syntax
HRESULT bindingName_CreateServiceProxy(
    __in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
    __in_ecount_opt(propertyCount) const WS_PROXY_PROPERTY* properties,
    __in const ULONG propertyCount,
    __deref_out WS_SERVICE_PROXY** serviceProxy,
    __in_opt WS_ERROR* error)
{
    return WsCreateServiceProxyFromTemplate(
      WS_CHANNEL_TYPE_REQUEST,    // this is fixed for http, requires input for TCP
      properties,     
      propertyCount, 
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),  
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_constraintName_POLICY_DESCRIPTION),
      serviceProxy,     
      error);     
}
```

``` syntax
HRESULT bindingName_CreateServiceEndpoint(
__in WS_bindingTemplateType_BINDING_TEMPLATE* templateValue,
__in_opt const WS_STRING* addressUrl,
__in bindingNameFunctionTable* functionTable,
__in WS_SERVICE_SECURITY_CALLBACK authorizationCallback,
__in const WS_SERVICE_ENDPOINT_PROPERTY* properties,
__in ULONG propertyCount,
__in WS_HEAP* heap,
  __deref_out WS_SERVICE_ENDPOINT** serviceEndpoint,
  __in_opt WS_ERROR* error)
{
  WS_SERVICE_CONTRACT serviceContract;
  serviceContract.contractDescription = &fileName.contracts.bindingName;
  serviceContract.defaultMessageHandlerCallback = NULL;
  serviceContract.methodTable = (const void *)functionTable;

  return WsCreateServiceEndpointFromTemplate(
      properties,
      propertyCount,
      addressUrl,    // service endpoint address
      WS_CHANNEL_TYPE_RESPONSE,    // this is fixed for http, requires input for TCP
      &serviceContract,
      authorizationCallback,
      heap,
      WS_bindingTemplateType_BINDING_TEMPLATE_TYPE,
      templateValue,
      sizeof(WS_bindingTemplateType_BINDING_TEMPLATE),
      &fileName.policies.bindingName,   // template description as generated in the stub file
      sizeof(WS_bindingTemplateType_POLICY_DESCRIPTION),
      serviceEndpoint,
      error);
}
```

## <a name="supported-policy-settings"></a>Поддерживаемые параметры политики

В следующей таблице перечислены все поддерживаемые типы шаблонов привязки, соответствующие привязки безопасности, необходимые для типа, структура шаблона, заполняемая приложением для типа, и тип описания сопоставления. Приложению необходимо заполнять структуру шаблона, тогда как разработчик приложения должен понимать, какие привязки безопасности необходимы в данной политике.



| [**\_ \_ тип шаблона привязки \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                                | Сочетания привязок безопасности                                                                                                                                                                                                                                                                                                               | Структура шаблона, заполняемая приложением                                                                                            | Описание политики                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ \_ тип шаблона привязки HTTP \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                          |                                                                                                                                                                                                                                                                                                                                             | [**\_ \_ шаблон привязки WS \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)                                                                              | [**\_ \_ Описание политики HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)                                                                              |
| [**\_ \_ \_ \_ тип шаблона привязки SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_ \_ \_ Привязка безопасности транспорта WS \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)                                                                                                                                                                                                                                                          | [**\_ \_ \_ шаблон привязки SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)                                                                     | [**\_ \_ \_ Описание политики WS HTTP \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)                                                                     |
| [**\_ \_ \_ \_ \_ тип шаблона привязки проверки ПОдлинности заголовка HTTP WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                            | [**\_ \_ \_ Привязка безопасности для проверки подлинности заголовка WS \_ HTTP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                                                                                                                   | [**\_ \_ \_ шаблон привязки проверки подлинности заголовка HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)                                                    | [**\_ \_ \_ Описание политики проверки подлинности заголовка WS HTTP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)                                                    |
| [**\_ \_ \_ \_ \_ \_ тип шаблона привязки проверки ПОдлинности заголовка SSL HTTP WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                       | [**Служба WS \_ Привязка безопасности \_ транспорта SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) и HTTPS [ **http Authentication \_ \_ \_ \_ \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)                                                                                                                                                            | [**\_ \_ \_ \_ шаблон привязки проверки подлинности заголовка SSL \_ http WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)                                           | [**\_ \_ \_ \_ Описание политики проверки подлинности заголовка WS \_ HTTP SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)                                           |
| [**\_ \_ \_ \_ \_ тип шаблона привязки имени пользователя SSL \_ http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**Служба WS \_ Привязка безопасности \_ транспорта \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) и [ **\_ \_ \_ \_ Привязка безопасности сообщений имени пользователя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                             | [**\_ \_ \_ шаблон привязки имени пользователя \_ SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)                                                  | [**\_ \_ \_ Описание политики имени пользователя \_ SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)                                                  |
| [**\_ \_ \_ \_ \_ \_ тип шаблона привязки SSL-апрек Kerberos \_ http WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**Служба WS \_ Привязка \_ \_ безопасности \_ транспорта SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) и [ **\_ \_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                                | [**\_ \_ шаблон SSL- \_ привязки Kerberos HTTP WS \_ апрек \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)                                     | [**\_ \_ \_ \_ \_ Описание политики WS-апрек SSL \_ Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)                                     |
| [**\_ \_ \_ тип шаблона привязки WS-TCP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                           |                                                                                                                                                                                                                                                                                                                                             | [**\_ \_ шаблон привязки WS \_ TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)                                                                                | [**\_ \_ Описание политики WS \_ TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)                                                                                |
| [**\_ \_ \_ \_ тип шаблона привязки WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                                     | [**\_ \_ \_ \_ Привязка безопасности транспорта WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)                                                                                                                                                                                                                                               | [**\_ \_ \_ шаблон привязки WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)                                                                     | [**\_ \_ \_ Описание политики WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)                                                                     |
| [**\_ \_ \_ \_ \_ тип шаблона привязки имени пользователя для протокола WS TCP SSPI \_**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                           | [**Служба WS \_ Привязка \_ безопасности \_ транспорта \_ \_ TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) и [ **\_ \_ \_ Безопасность \_ сообщений имени пользователя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)                                                                                                                                                  | [**\_ \_ \_ шаблон привязки имени пользователя \_ для WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)                                                  | [**\_ \_ \_ Описание политики имени пользователя \_ для WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)                                                  |
| [**\_ \_ \_ \_ \_ \_ тип шаблона привязки \_ WS TCP SSPI Kerberos апрек**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)                    | [**Служба WS \_ Привязка \_ безопасности \_ транспорта \_ \_ TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) и [ **\_ \_ \_ \_ \_ Привязка безопасности сообщений WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)                                                                                                                                     | [**\_ \_ шаблон привязки WS TCP SSPI \_ Kerberos \_ апрек \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)                                     | [**\_ \_ Описание политики WS TCP SSPI \_ Kerberos \_ апрек \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)                                     |
| [**\_ \_ \_ \_ \_ \_ \_ тип шаблона привязки контекста безопасности имени пользователя \_ SSL HTTP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**Служба WS \_ Привязка безопасности \_ транспорта \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) и [**\_ \_ \_ \_ \_ Привязка безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) с [**помощью \_ \_ \_ \_ привязки безопасности сообщений имени пользователя**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) в канале начальной загрузки                         | [**\_ \_ \_ \_ \_ \_ шаблон привязки контекста безопасности имени пользователя SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)              | [**\_ \_ \_ \_ \_ \_ Описание политики контекста безопасности имени пользователя SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)              |
| [**\_ \_ \_ \_ \_ \_ \_ \_ тип шаблона привязки контекста безопасности \_ WS HTTP SSL Kerberos апрек**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**Служба WS \_ Привязка безопасности \_ транспорта \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) и [**\_ \_ \_ \_ \_ Привязка безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) с [**помощью \_ \_ \_ \_ \_ привязки безопасности сообщений WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) в канале начальной загрузки            | [**\_ \_ \_ \_ \_ \_ \_ шаблон привязки протокола безопасности \_ HTTP SSL Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template) | [**\_ \_ \_ \_ \_ \_ \_ Описание политики контекста безопасности \_ WS HTTP SSL Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description) |
| [**\_ \_ \_ \_ \_ \_ \_ тип шаблона привязки контекста безопасности имени пользователя \_ для WS TCP SSPI**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)        | [**Служба WS \_ Привязка \_ безопасности \_ транспорта \_ \_ TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) и [**\_ \_ \_ \_ \_ Привязка безопасности сообщений контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) с [**помощью \_ \_ \_ \_ привязки безопасности сообщений имени пользователя**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) в канале начальной загрузки              | [**\_ \_ \_ \_ \_ \_ шаблон привязки контекста безопасности имени пользователя \_ для WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)              | [**\_ \_ \_ \_ \_ \_ Описание политики контекста безопасности имени пользователя \_ для WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)              |
| [**\_ \_ \_ \_ \_ \_ \_ \_ тип шаблона привязки контекста безопасности \_ WS TCP SSPI Kerberos апрек**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) | [**Служба WS \_ Привязка \_ безопасности \_ транспорта \_ \_ TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding) и [**\_ \_ \_ \_ безопасность сообщений \_ контекста безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) с помощью [**\_ \_ \_ \_ \_ привязки безопасности сообщений WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) в канале начальной загрузки | [**\_ \_ \_ \_ \_ \_ \_ шаблон привязки контекста безопасности \_ для WS TCP SSPI Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template) | [**\_ \_ \_ \_ \_ \_ \_ Описание политики контекста безопасности \_ WS TCP SSPI Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description) |



 

Например, [**\_ \_ \_ \_ \_ тип шаблона привязки SSL HTTP WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type) указывает, что входная политика для привязки указывает транспорт HTTP и [**\_ \_ \_ \_ привязку безопасности транспорта WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Приложению необходимо заполнить структуру [**\_ \_ \_ \_ шаблона привязки SSL HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template) перед вызовом вспомогательных подпрограмм, а описание политики сопоставления — [**\_ \_ \_ \_ Описание политики WS HTTP SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description). В частности, раздел Binding в WSDL содержит следующие сегменты:

``` syntax
<wsp:Policy...>
  <sp:TransportBinding...>
    <wsp:Policy...>
      <sp:TransportToken...>
        <wsp:Policy...>
          <sp:HttpsToken.../>
        </wsp:Policy...>
      </sp:TransportToken...>
    </wsp:Policy>
  </sp:TransportBinding...>
</wsp:Policy>
```

``` syntax
<wsdl:binding...>
<soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

## <a name="security-context-support"></a>Поддержка контекста безопасности

В [контексте безопасности](security-context.md)создается канал начальной загрузки для установления безопасного диалога в канале службы. Всутил поддерживает только сценарий, в котором загрузочный канал совпадает с каналом службы с теми же свойствами канала и свойствами безопасности. Для привязки сообщений контекста безопасности требуется безопасность транспорта. всутил поддерживает загрузочные каналы с другими привязками безопасности сообщений, но поддерживает только контекст безопасности только в качестве привязки безопасности сообщений в канале службы без сочетания с другими привязками безопасности сообщений. Разработчики могут поддерживать эти сочетания за пределами поддержки шаблонов политик.

Следующее перечисление является частью поддержки политики:

-   [**\_ \_ тип шаблона привязки \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_binding_template_type)

Следующие функции являются частью поддержки политик:

-   [**вскреатесервицеендпоинтфромтемплате**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceendpointfromtemplate)
-   [**вскреатесервицепроксифромтемплате**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxyfromtemplate)

Следующие структуры являются частью поддержки политик:

-   [**\_ \_ шаблон привязки WS \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_binding_template)
-   [**\_ \_ \_ шаблон привязки проверки подлинности заголовка HTTP \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_binding_template)
-   [**\_ \_ \_ Описание политики проверки подлинности заголовка WS HTTP \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_policy_description)
-   [**\_ \_ \_ \_ \_ \_ Описание политики привязки безопасности для проверки ПОдлинности HTTP-заголовка WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_policy_description)
-   [**\_ \_ \_ \_ \_ шаблон привязки безопасности для проверки подлинности HTTP-заголовка WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_template)
-   [**\_ \_ Описание политики HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_policy_description)
-   [**\_ \_ \_ шаблон привязки SSL HTTP \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_binding_template)
-   [**\_ \_ \_ \_ шаблон привязки проверки подлинности заголовка SSL \_ http WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_binding_template)
-   [**\_ \_ \_ \_ Описание политики проверки подлинности заголовка WS \_ HTTP SSL \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_header_auth_policy_description)
-   [**\_ \_ шаблон SSL- \_ привязки Kerberos HTTP WS \_ апрек \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_binding_template)
-   [**\_ \_ \_ \_ \_ Описание политики WS-апрек SSL \_ Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_policy_description)
-   [**\_ \_ \_ \_ \_ \_ \_ шаблон привязки протокола безопасности \_ HTTP SSL Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_binding_template)
-   [**\_ \_ \_ \_ \_ \_ \_ Описание политики контекста безопасности \_ WS HTTP SSL Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_kerberos_apreq_security_context_policy_description)
-   [**\_ \_ \_ Описание политики WS HTTP \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_policy_description)
-   [**\_ \_ \_ шаблон привязки имени пользователя \_ SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_binding_template)
-   [**\_ \_ \_ Описание политики имени пользователя \_ SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_policy_description)
-   [**\_ \_ \_ \_ \_ \_ шаблон привязки контекста безопасности имени пользователя SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_binding_template)
-   [**\_ \_ \_ \_ \_ \_ Описание политики контекста безопасности имени пользователя SSL \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_ssl_username_security_context_policy_description)
-   [**\_ \_ \_ \_ \_ \_ Описание политики привязки безопасности сообщений \_ WS Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_policy_description)
-   [**\_ \_ \_ \_ \_ шаблон привязки безопасности сообщений WS Kerberos \_ апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_template)
-   [**\_ \_ \_ \_ \_ \_ Описание политики привязки безопасности сообщений контекста \_ безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_policy_description)
-   [**\_ \_ \_ \_ \_ шаблон привязки безопасности сообщений контекста \_ безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_template)
-   [**\_ \_ \_ \_ \_ Описание политики привязки безопасности контекста \_ безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_policy_description)
-   [**\_ \_ \_ \_ шаблон привязки безопасности контекста безопасности \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_security_binding_template)
-   [**\_ \_ \_ \_ \_ Описание политики привязки безопасности транспорта \_ SSL WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_policy_description)
-   [**\_ \_ \_ \_ шаблон привязки безопасности транспорта \_ WS-SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_template)
-   [**\_ \_ \_ \_ \_ Описание политики привязки безопасности транспорта \_ WS SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_sspi_transport_security_binding_policy_description)
-   [**\_ \_ шаблон привязки WS \_ TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_binding_template)
-   [**\_ \_ Описание политики WS \_ TCP**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_policy_description)
-   [**\_ \_ \_ шаблон привязки WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_binding_template)
-   [**\_ \_ шаблон привязки WS TCP SSPI \_ Kerberos \_ апрек \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_binding_template)
-   [**\_ \_ Описание политики WS TCP SSPI \_ Kerberos \_ апрек \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_policy_description)
-   [**\_ \_ \_ \_ \_ \_ \_ шаблон привязки контекста безопасности \_ для WS TCP SSPI Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_binding_template)
-   [**\_ \_ \_ \_ \_ \_ \_ Описание политики контекста безопасности \_ WS TCP SSPI Kerberos апрек**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_kerberos_apreq_security_context_policy_description)
-   [**\_ \_ \_ Описание политики WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_policy_description)
-   [**\_ \_ \_ \_ \_ шаблон привязки безопасности транспорта WS TCP \_ SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_template)
-   [**\_ \_ \_ шаблон привязки имени пользователя \_ для WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_binding_template)
-   [**\_ \_ \_ Описание политики имени пользователя \_ для WS TCP SSPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_policy_description)
-   [**\_ \_ \_ \_ \_ \_ шаблон привязки контекста безопасности имени пользователя \_ для WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_binding_template)
-   [**\_ \_ \_ \_ \_ \_ Описание политики контекста безопасности имени пользователя \_ для WS TCP SSPI**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_username_security_context_policy_description)
-   [**\_ \_ \_ \_ \_ Описание политики привязки безопасности сообщений \_ имени пользователя WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_policy_description)
-   [**\_ \_ \_ \_ шаблон привязки безопасности сообщений имени пользователя WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_template)

 

 




