---
title: Конфигурация подключаемого модуля службы WinRM
description: Подключаемый модуль служба удаленного управления Windows (WinRM) должен быть зарегистрирован в каталоге WinRM, чтобы инфраструктура динамически определила набор доступных подключаемых модулей и URI ресурсов, которые они поддерживают.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104339605"
---
# <a name="winrm-service-plug-in-configuration"></a>Конфигурация подключаемого модуля службы WinRM

Подключаемый модуль служба удаленного управления Windows (WinRM) должен быть зарегистрирован в каталоге WinRM, чтобы инфраструктура динамически определила набор доступных подключаемых модулей и [*URI ресурсов*](windows-remote-management-glossary.md) , которые они поддерживают. Все [*URI ресурсов*](windows-remote-management-glossary.md) для подключаемых модулей WinRM должны соответствовать формату, определенному в RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ). Настройка выполняется с помощью основной службы WinRM.

Следующая команда регистрирует конфигурацию подключаемого модуля в службе WinRM:

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> Чтобы предоставить новые зарегистрированные подключаемые модули, необходимо перезапустить службу WinRM.

Конфигурация подключаемого модуля указывается в формате XML. Пример.

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



В следующем списке описаны XML-элементы более подробно и за ним следует схема конфигурации, указанная в виде XSD.

<dl> <dt>

<span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**Плугинконфигуратион** / **Оператионсконфигуратион**
</dt> <dd>

Указывает имя файла подключаемого модуля операций. Все переменные среды, помещаемые в эту запись, будут развернуты в контексте пользователя при последующем запросе. У каждого пользователя может быть другая версия одной и той же переменной среды, поэтому каждый пользователь может использовать другой подключаемый модуль. Эта запись не может быть пустой и должна указывать на допустимый подключаемый модуль.

</dd> <dt>

<span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**Плугинконфигуратион** / **Имя**
</dt> <dd>

Указывает отображаемое имя, используемое для подключаемого модуля. Если из подключаемого модуля возвращается ошибка, то это имя помещается в XML-код ошибки, который возвращается клиентскому приложению. Это имя может быть на любом языке.

</dd> <dt>

<span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**Плугинконфигуратион** / **Архитектура**
</dt> <dd>

Указывает, является ли подключаемый модуль операций 32-разрядным или 64-битным. Если этот элемент не указан, по умолчанию будет установлено значение "32" в системах x86, а в 64-разрядных системах — "64". Для систем x86 единственным допустимым значением является "32". Если значение равно "32" в 64-разрядной системе, при вводе сведений о **имени файла** необходимо учитывать перенаправление WOW64. Базовая файловая система будет использовать перенаправление WOW64 для преобразования system32 в syswow64. Например, если **filename** имеет значение "% WINDIR% \\ system32 \\myplugin.dll" и **архитектура** — "32", фактический файл подключаемого модуля находится в папке "% WINDIR% \\ SysWOW64 \\myplugin.dll".

</dd> <dt>

<span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**Плугинконфигуратион** / **Ксмлрендерингтипе**
</dt> <dd>

Настраивает формат, в котором XML передается в подключаемые модули через [**объект \_ данных WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) . Доступны следующие типы.

<dl> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>Полнотекстовым
</dt> <dd>

Входящие XML-данные содержатся в \_ \_ \_ текстовой структуре WSMan типа данных, которая представляет XML как **пквстр** буфер памяти.

</dd> <dt>

<span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>Чтения
</dt> <dd>

Входящие XML-данные содержатся в \_ \_ \_ \_ структуре модуля чтения XML типа данных WSMan WS \_ , которая представляет XML как объект **XmlReader** , который определен в файле заголовка WebService. h.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**Плугинконфигуратион** / **Инитиализатионксмл**
</dt> <dd>

Этот узел является необязательным и позволяет подключаемому модулю настроить дополнительный XML, который будет передан методу [**всманплугинстартуп**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup). Большинству подключаемых модулей эти дополнительные сведения не понадобятся, но если подключаемый модуль должен использоваться в нескольких сценариях, требующих другой семантики времени выполнения, этот XML предоставит подключаемому модулю такую гибкость.

</dd> <dt>

<span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**Плугинконфигуратион** / **Ресурсы**
</dt> <dd>

Указывает список [*URI ресурсов*](windows-remote-management-glossary.md), поддерживаемых этим подключаемым модулем. Необходимо указать по меньшей мере одну запись **ResourceUri**; в противном случае XML будет отклонен.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс**
</dt> <dd>

Представляет одну конфигурацию [*URI ресурса*](windows-remote-management-glossary.md).

> [!Note]  
> Для атрибута **суппортсоптионс** можно задать значение false. Если для **суппортсоптионс** задано значение false, этот атрибут не указывается при перечислении ресурса.

 

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс** / **ResourceUri**
</dt> <dd>

Указывает один [*URI ресурса*](windows-remote-management-glossary.md) либо в полной, либо в виде частичной строки соответствия на основе атрибута **ExactMatch** . Если **ExactMatch** отсутствует, по умолчанию используется **значение false**, означающее, что обработчик WinRM SOAP выполняет частичное сопоставление с началом *URI ресурса* , а при наличии совпадения передает его в подключаемый модуль. Атрибут **суппортсоптионс** можно указать, если этому *URI ресурса* разрешено передавать любые параметры. По умолчанию параметры не поддерживаются, и если они имеются в клиентском запросе, возвращается ошибка. Если параметры поддерживаются подключаемым модулем, то важно, чтобы подключаемый модуль возвращал правильную ошибку, если существует параметр, в котором подключаемый модуль не понимает, когда для флага **MustUnderstand** установлено значение **true**.

</dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс** / **Возможности**
</dt> <dd>

Указывает возможность, доступную в этом [*URI ресурса*](windows-remote-management-glossary.md). Для каждого поддерживаемого типа операции будет существовать одна запись. Доступны следующие варианты:

<dl> <dt>

<span id="Get"></span><span id="get"></span><span id="GET"></span>Получить
</dt> <dd>

Операции Get поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** используется, если операция get поддерживает концепцию. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение false. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Put"></span><span id="put"></span><span id="PUT"></span>PUT
</dt> <dd>

Операции размещения поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** используется, если операция размещения поддерживает концепцию. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>Создания
</dt> <dd>

Операции создания поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** используется, если операция создания поддерживает концепцию. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Удален
</dt> <dd>

Операции Delete поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** используется, если операция удаления поддерживает концепцию. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Вызвать
</dt> <dd>

Операции Invoke поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** не поддерживается для операций Invoke и должен иметь значение false. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Перечислить
</dt> <dd>

Операции перечисления поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** не поддерживается для операций перечисления и должен иметь значение **false**. Атрибут **суппортфилтеринг** является допустимым, и если подключаемый модуль поддерживает фильтрацию, для этого атрибута необходимо задать значение **true**. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Наблюдателя
</dt> <dd>

Операции подписки поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** не поддерживается для операций подписки и должен иметь значение **false**. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**. Эта возможность недопустима для *URI ресурса* , если также поддерживаются операции оболочки.

</dd> <dt>

<span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Консоль
</dt> <dd>

Операции оболочки поддерживаются в [*URI ресурса*](windows-remote-management-glossary.md). Атрибут **суппортфрагмент** не поддерживается для операций оболочки и должен иметь значение **false**. Атрибут **суппортфилтеринг** является недопустимым и должен иметь значение **false**. Эта возможность недопустима для *URI ресурса* , если также поддерживается любая другая операция. Если для *универсального кода ресурса (URI)* настроена возможность работы с оболочкой, то операции получения, размещения, создания, удаления, вызова и перечисления обрабатываются внутри службы WinRM для управления оболочками. В результате подключаемый модуль не может работать с самими операциями.

</dd> </dl> </dd> <dt>

<span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**Плугинконфигуратион** / **Ресурсы** / **Ресурс** / **Безопасность**
</dt> <dd>

Этот элемент определяет дескриптор безопасности (через атрибут **SDDL** ), который должен применяться для определения доступа к определенному [*URI ресурса*](windows-remote-management-glossary.md) (через атрибут **URI** ). Если **ExactMatch** отсутствует, элемент **безопасности** по умолчанию имеет **значение false**, что означает, что **SDDL** применяется ко всем *URI ресурсов* , которые используют **универсальный код ресурса (URI)** в качестве префикса. Если для **ExactMatch** задано значение true, то **SDDL** применяется только к указанному точному **URI** . При наличии нескольких записей **безопасности** , которые могут применяться к определенным *URI ресурса*, для определения соответствующего **SDDL** используется наиболее длинное совпадение префиксов. В результате совпадения с наибольшим префиксом, если запись **URI** точного соответствия существует, она всегда будет выбрана в качестве соответствующего элемента безопасности.

</dd> </dl>

Ниже приведена схема конфигурации подключаемого модуля, заданная как XSD.

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




