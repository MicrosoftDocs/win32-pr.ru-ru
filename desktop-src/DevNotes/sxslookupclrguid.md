---
description: Извлекает имя класса и другие сведения, связанные с данным идентификатором GUID в манифесте компонента.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Функция Сксслукупклргуид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 516ba97eb70defdbc6f92efa5c65e6d23246fe67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465601"
---
# <a name="sxslookupclrguid-function"></a>Функция Сксслукупклргуид

Извлекает имя класса и другие сведения, связанные с данным идентификатором GUID в манифесте компонента. эта функция используется только при реализации низкоуровневого управляемого неуправляемого взаимодействия в платформа .NET Framework. дополнительные сведения о взаимодействии управляемого и неуправляемого кода см. в разделе "взаимодействие с неуправляемым кодом" раздела платформа .NET Framework SDK, а также [изолированные приложения и параллельные сборки](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

## <a name="syntax"></a>Синтаксис


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Сочетание следующих флагов (ноль или более).



| Значение                                                                                                                                                                                                                                                                                             | Значение                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SxS \_ УТОЧНЯющий запрос \_ CLR \_ GUID \_ USE \_ акткткс**</dt> <dt>0x00000001</dt> </dl>              | Если этот флаг установлен, параметр *хакткткс* должен содержать обработчик контекста активации, возвращаемый функцией [**креатеакткткс**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Если этот флаг не установлен, параметр *хакткткс* игнорируется и **сксслукупклргуид** ищет активный в данный момент контекст активации (функция [**активатеакткткс**](/windows/win32/api/winbase/nf-winbase-activateactctx) используется, чтобы активировать контекст активации).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SxS \_ УТОЧНЯющий запрос GUID поиска- \_ \_ идентификатора \_ \_ CLR**</dt> <dt>0x00010000</dt> </dl>  | Если этот флаг установлен, **сксслукупклргуид** выполняет поиск суррогата.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SxS \_ УТОЧНЯющий запрос GUID поиска для \_ \_ \_ \_ \_ класса CLR**</dt> <dt>0x00020000</dt> </dl> | Если этот флаг установлен, **сксслукупклргуид** выполняет поиск класса.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SxS \_ Поиск \_ по \_ идентификатору GUID CLR \_ найти \_ любой**</dt> <dt>0x00030000</dt> </dl>                    | Это сочетание флагов поиска **SxS в \_ \_ CLR \_ GUID \_ Find \_ суррогат** и SxS Lookup CLR " **\_ \_ \_ \_ Find \_ CLR \_** ". Если заданы оба параметра, **сксслукупклргуид** сначала ищет суррогат, и только если он не находит его, а затем выполняет поиск класса.<br/>                                                                                                                                                |



 

</dd> <dt>

*пклсид* \[ окне\]
</dt> <dd>

Указатель на идентификатор GUID, по которому будет производиться поиск сведений о взаимооперациях в контексте активации. Этот параметр не может иметь **значение NULL**.

</dd> <dt>

*хакткткс* \[ в необязательное\]
</dt> <dd>

Если в параметре *dwFlags* задано использование флага **\_ \_ \_ \_ \_ Акткткс в таблице GUID поиска SxS** , то *Хакткткс* должен содержать обработчик контекста активации, возвращаемый функцией [**креатеакткткс**](/windows/win32/api/winbase/nf-winbase-createactctxa) . В противном случае *хакткткс* игнорируется.

</dd> <dt>

*пваутпутбуффер* \[ в, out, необязательно\]
</dt> <dd>

Указатель на буфер, в который копируются возвращаемые сведения. Этот параметр может иметь значение NULL только в том случае, если параметр *кбаутпутбуффер* имеет нулевое значение. Данные, помещаемые в этот буфер при выходе (если таковые имеются), состоят из структуры **\_ \_ \_ CLR со сведениями о GUID SxS** , за которыми следуют дополнительные строковые данные. Дополнительные сведения см. в разделе "Примечания" ниже.

</dd> <dt>

*кбаутпутбуффер* \[ окне\]
</dt> <dd>

Размер в байтах буфера, на который указывает параметр *пваутпутбуффер* .

</dd> <dt>

*пкбаутпутбуффер* \[ заполняет\]
</dt> <dd>

Указатель на переменную, в которой при выходе помещается размер возвращаемых данных (в байтах). Если параметр *кбаутпутбуффер* равен нулю или размер выходного буфера меньше, чем размер возвращаемых данных, то **сксслукупклргуид** завершается ошибкой, а [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает ошибку, **\_ недостаточную для \_ буфера**. В этом случае используйте значение в переменной, на которую указывает *пкбаутпутбуффер* , для выделения достаточного размера буфера, а затем вызовите **сксслукупклргуид** еще раз, чтобы получить нужную информацию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если успешно, или **false** в противном случае. Для получения дополнительных сведений об ошибке вызовите [ **GetLastError** .](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Комментарии

Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Управляемые компоненты могут объявлять себя как поддерживающие управляемые "сборки взаимодействия", что позволяет неуправляемому потребителю компонента Win32 ссылаться на объявляемую сборку. Потребитель компонента может взаимодействовать с управляемым компонентом, вызывая [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для идентификатора GUID. уровень взаимодействия направляет запрос на создание объекта в платформа .NET Framework, создает экземпляр управляемого объекта и возвращает указатель интерфейса.

**сксслукупклргуид** позволяет платформам извлекать информацию, связанную с данным идентификатором GUID, в манифесте компонента, например имя его класса .net, какая версия платформа .NET Framework требуется и какая сборка узла, в которой он находится. Управляемые компоненты публикуют сборку взаимодействия, содержащую несколько инструкций, связывающих идентификаторы GUID с именами сборок и типов, а среда выполнения .NET — построение экземпляров управляемых объектов при вызове [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

Ниже приведен пример манифеста компонента, объявляющего GUID CLR и суррогат CLR, который **сксслукупклргуид** может искать:

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

Поставщик взаимодействий вызовет **сксслукупклргуид** с указателем на GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" и получит в результате возврата имени класса "мисамплесуррогате", требуемой версии среды выполнения "1.0.3055" и текстового удостоверения "DotNet. Sample. суррогаты, Version =" 1.0.0.0 ", Type =" Interop "для компонента размещения.

Эти возвращаемые сведения должны содержаться и (или) ссылаться на структуру **\_ \_ \_ CLR со сведениями об идентификаторах SxS** , объявленной следующим образом.

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

Члены этой структуры содержат следующие сведения.




| Член | Описание | 
|--------|-------------|
| <span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>кбсизе</strong><br /> | Содержит размер структуры SXS_GUID_INFORMATION_CLR (это позволяет увеличить структуру в более поздних версиях).<br /> | 
| <span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br /> | Содержит одно из следующих двух значений флагов: <br /><ul><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): указывает, что указанный GUID был связан с "суррогатом".</li><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): указывает, что указанный GUID был связан с классом.</li></ul> | 
| <span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>пквсзрунтимеверсион</strong><br /> | Указывает на строку расширенных символов, завершающуюся нулем, которая определяет версию среды выполнения, указанную в манифесте узла для этого класса.<br /> | 
| <span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>пквсзтипенаме</strong><br /> | Указывает на строку расширенных символов, заканчивающуюся нулем, которая содержит имя класса .NET, связанного с указанным GUID.<br /> | 
| <span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>пквсзассемблидентити</strong><br /> | Указывает на строку расширенных символов, завершающуюся нулем, которая содержит текстовое удостоверение сборки, в которой размещен этот класс. дополнительные сведения о текстовом удостоверении см. в разделе "указание полных имен типов" раздела "определение типа данных во время выполнения" раздела "программирование с помощью платформа .NET Framework" в пакете SDK для платформа .NET Framework.<br /> | 




 

неуправляемое приложение может использовать возвращенную информацию, чтобы загрузить правильную версию платформа .NET Framework, загрузить сборку, определенную элементом **пквсзассемблидентити** , а затем создать экземпляр класса с именем с помощью элемента **пквсзтипенаме** .

## <a name="examples"></a>Примеры

Используйте динамическую компоновку, как показано ниже, чтобы вызвать функцию **сксслукупклргуид** :


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Изолированные приложения и параллельные сборки](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**креатеакткткс**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**активатеакткткс**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
