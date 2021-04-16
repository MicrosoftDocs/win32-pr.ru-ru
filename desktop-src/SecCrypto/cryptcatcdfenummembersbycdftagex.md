---
description: Перечисляет отдельные элементы файла в разделе Каталогфилес файла определения каталога (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Функция Крипткаткдфенуммемберсбикдфтажекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541002"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a>Функция Крипткаткдфенуммемберсбикдфтажекс

\[Функция **крипткаткдфенуммемберсбикдфтажекс** доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Функция **крипткаткдфенуммемберсбикдфтажекс** перечисляет отдельные элементы File в разделе **каталогфилес** файла определения каталога (CDF). **Крипткаткдфенуммемберсбикдфтажекс** вызывается [макекат](makecat.md).

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкдф* \[ окне\]
</dt> <dd>

Указатель на структуру [**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*пвсзпревкдфтаг* \[ в, out\]
</dt> <dd>

Указатель на строку, **завершающуюся нулем,** которая определяет элемент файла каталога.

</dd> <dt>

*пфнпарсиррор* \[ окне\]
</dt> <dd>

Указатель на определяемую пользователем функцию для обработки ошибок синтаксического анализа файла.

</dd> <dt>

*ппмембер* \[ окне\]
</dt> <dd>

Указатель на структуру [**крипткатмембер**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) , содержащую сведения об элементе файла.

</dd> <dt>

*фконтинуеонеррор* \[ окне\]
</dt> <dd>

Значение типа, указывающее, следует ли размещать в памяти ссылку на последний перечислимый элемент.

</dd> <dt>

*пвресервед* \[ окне\]
</dt> <dd>

Этот параметр зарезервирован; не используйте его.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

После успешного выполнения эта функция возвращает указатель на строку, завершающуюся **нулем**, которая определяет элемент файла в разделе **каталогфилес** CDF. При сбое функция **крипткаткдфенуммемберсбикдфтажекс** возвращает **пустой** указатель.

## <a name="remarks"></a>Комментарии

Обычно эта функция вызывается в цикле для перечисления всех элементов файла каталога в CDF. Перед входом в цикл задайте  для Пвсзпревкдфтаг **значение NULL**. Функция возвращает указатель на первый элемент. Задайте *пвсзпревкдфтаг* в качестве возвращаемого значения функции для последующих итераций цикла.

## <a name="examples"></a>Примеры

В следующем примере показана правильная последовательность назначений для параметра *пвсзпревкдфтаг* ( `pwszMemberTag` ).


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[макекат](makecat.md)
</dt> <dt>

[**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**крипткатмембер**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
